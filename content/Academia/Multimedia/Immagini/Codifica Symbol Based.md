---
tags:
  - Academia/Multimedia/Immagini/Codifiche
---
In una codifica basata su token, un'immagine viene rappresentata come una serie di sottoimmagini ricorrenti, chiamati simboli.
Ciascun simbolo è memorizzato come un _dizionario di simbolo_, e l'immagine è codificata come un insieme di terzine ${(x_{1},y_{1},t_{1}),(x_{2},y_{2},t_{2}),\dots}$ in cui ciascuna coppia $(x_{i},y_{i})$ determina la posizione di un simbolo nell'immagine, e il token $t_{i}$ è l'indirizzo del simbolo della sottoimmagine nel dizionario.

Immagazzinando solo una volta i simboli ripetuti si possono comprimere significativamente le immagini, dove i simboli sono spesso delle vere e proprie bitmap ripetute più volte.

Riassumento: per ogni $t$, corrisponderà una matrice $A$ (cioè un simbolo) all'interno della matrice $I$ (l'immagine completa) alle coordinate specificate.

![[Pasted image 20231210214443.png|512]]