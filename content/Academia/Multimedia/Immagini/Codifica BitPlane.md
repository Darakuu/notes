---
tags:
  - Academia/Multimedia/Immagini/Codifiche
---
# Variante Base
Le tecniche [[Codifica RLE|RLE]] e [[Codifica Symbol Based|Symbol Based]] possono essere applicate alle immagini che hanno più di due intensità attraverso l'elaborazione dei loro singoli bit-plane.

Questa codifica si basa sul concetto di scomposizione di una immagine nei suoi singoli bitplane, cioè in una serie di immagini binarie, e compressione mediante un altro algoritmo conosciuto.

Le intensità di un'immagine grayscale a $m$ bit possono essere rappresentate con il seguente polinomio a base 2:

$a_{m-1}2^{m-1}+a_{m-2}2^{m-2}+\dots+a_{1}2^{1}+a_{0}2^{0}$

L'immagine si scompone separando gli $m$ coefficienti del polinomio in $m$ piani a $1$ bit.
![[Pasted image 20231210215540.png|Ad ogni valore di grigio corrisponde una rappresentazione in numeri binari (8 bit) come indicato nella figura a destra|512]]

L'immagine a 8 bit è quindi scomposta in 8 piani ad 1 bit. Il piano 1 contiene il bit meno significativo di tutti i pixel dell'immagine

![[Pasted image 20231210215715.png|384]]

I piani di ordine più alto contengono le aree più uniformi e con meno dettagli dell'immagine.

I piani di ordine più basso contengono i dettagli dell'immagine.

![[Pasted image 20231210215903.png|128]]

La scomposizione in piani di bit ha lo svantaggio che se si ha la presenza di piccole variazioni di intensità, questa si ripercuote su tutti i bitplane.
Se un pixel ha ad esempio intensità 127 (01111111) e il suo adiacente ha intensità 128 (10000000) allora la transizione tra 0 e 1 si ripercuote su tutti i piani di bit. Per risolvere questo problema si usa la variante con XOR della scomposizione bitplanes:
# Variante con XOR e Gray Code

Il Gray Code a m bit $g_{m-1}\dots g_{2}g_{1}g_{0}$ che corrisponde al numero binario $a_{m-1}\dots a_{2}a_{1}a_{0}$ può essere calcolato da:
$g_{i}=a_{i}\oplus a_{i+1} \quad 0\leq i\leq m-2$
$g_{m-1} = a_{m-1}$

dove $\oplus$ è lo XOR.

>[!definition] Proprietà:
>Ogni codeword differisce dalla precedente solo per un bit

Bit: $\qquad\qquad\quad  127:\text{  01111111}\quad 128:\text{10000000}$  
Gray code: $\qquad 127:\text{01000000} \quad 128:\text{11000000}$

solo il piano di ordine più alto è influenzato