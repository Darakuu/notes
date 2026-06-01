---
tags:
  - Academia/GameTheory/Method
aliases:
  - IESDS
---
## IESDS

> [!application] Steps

1. $x^0_{1}=x_{i}\  \forall\ i \in N, k=0$
2. Si Consideri il gioco $T^k=(N,(x_{i}^k)_{i \in N},(f_{i})_{i\in N})$
3. $\forall i \in N$, si rimuovono le strategie dominate:
	1. $x_{i}^{k+1}=\{ x \in X^k_{i}\ ,\ x_{i} \text{ non è strettamente dominante}\}$
4. $x^{k+1}=\prod_{i \in N}x_{i}^{k+1}$
5. IF: $\mid x^{k+1}\mid\ \leq\  1 \implies \text{STOP}$, problema risolto.
	1. ELSE: tutte le strategie di $x^{k+1}$ sono possibili.
6. $k++$ , vai a passo $2$.

> [!info] Osservazione
> Questo metodo è basato sulla **FORTE** assumption della common knowledge di tutti i player.
> Inoltre, a volte non c'è una soluzione al gioco


> [!info] Nota Bene
> L'ordine delle eliminazioni non conta


### Esempio

![[Pasted image 20241017084024.png|400]]

Diventa, dopo alcune comparison:

![[Pasted image 20241017084105.png|400]]

L'ordine per arrivare a questo particolare risultato è:

1. Player 1: UP - CENTER $\implies$ UP è dominata da CENTER per il Player 1, si rimuove la riga associata ad UP.
2. Player 1: CENTER - DOWN $\implies$ nulla è dominato, la riga resta.
3. Player 2: LEFT - RIGHT $\implies$ RIGHT è dominata da LEFT, rimuoviamo la colonna associata a RIGHT.
4. Ripetiamo la comparison CENTER - DOWN, a questo punto è facile vedere che CENTER è sempre peggio. Siamo arrivato alla soluzione (DOWN , LEFT) = (6,5)

