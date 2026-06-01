---
tags:
  - Academia/Multimedia/Immagini/Segmentazione
  - Academia/Multimedia/Immagini/Segmentazione/EdgeBased
---
Basato sull'[[Operatore Laplaciano]].
Si usa il laplaciano in connessione con un filtro di smoothing, ancora una volta una gaussiana, realizzando un operatore detto Laplaciano della Gaussiana o LoG (in figura una sezione trasversale ottenuta per σ=1)
![[Pasted image 20231211020619.png]]
Si può dimostrare che il valore medio della funzione è 0, e lo stesso avviene per il risultato della sua convoluzione con una immagine. 
La tipica forma a sombrero (in 3D) indica inoltre che la convoluzione dell’operatore LoG con una immagine provoca un blurring (di entità proporzionale a σ) dell’immagine stessa, e quindi ha un effetto positivo in termini di riduzione del rumore.
Il vantaggio principale offerto dall’operatore LoG resta comunque quello legato alla presenza degli Zero Crossing.
Gli Zero Crossing, cioè i confini tra zone nere e bianche nell’immagine binaria, diventano più individuabili.