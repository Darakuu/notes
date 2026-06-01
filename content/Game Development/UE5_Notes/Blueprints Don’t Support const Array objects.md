---
tags:
  - GameDev/UE5/programming
---

Let's say we have a TArray defined as follows:
`TArray<TObjectPtr<const SomeUObject>> Objects;`

If we then want to return the (mutable) array, as a BlueprintCallable function, we cannot do that easily (by reference):

```cpp
const TArray<SomeUObject*>& OurClass::GetObjectsArray()
{
	return Objects; // Won't compile!
}

```

We'll also get gnarly errors which might not be obvious at first glance.

What we have to do instead, is to return a mutable copy of the array to the blueprint API. We can also have a native function that passes the array by reference, if we want.

```cpp
TArray<SomeUObject*> OurClass::GetObjects() const  
{  
    TArray<SomeUObject*> OutQueue;  
    OutQueue.Reserve(Objects.Num());  
  
    for (const TObjectPtr<const SomeUObject>& Object : Objects)  
    {  
        OutQueue.Add(const_cast<SomeUObject*>(Object.Get())); // We can "safely" cast the const away.
    }  
  
    return OutQueue;  
}
```

This is especially useful if you work with Data Assets (which are intended to be read only), and have not setup a Data Asset <-> Instance system.