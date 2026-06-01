---
tags:
  - Academia/Multimedia/Immagini/Segmentazione
  - Academia/Multimedia/Immagini/Segmentazione/EdgeBased
---
La determinazione degli zero crossing della derivata seconda della $f(x,y)$ localizza con precisione i contorni dell’immagine, mentre il **segno** della derivata seconda permette di stabilire l’**appartenenza** di un pixel al versante **scuro** o al versante **chiaro** di un contorno.

Un modo molto comune di effettuare le operazioni di derivata seconda di una $f(x,y)$ in un punto è quello di calcolare il laplaciano in quel punto. Ricordiamo che data una funzione $f(x,y)$, il laplaciano di $f$ in $(x,y)$ è definito come:

$L(x,y)=\nabla^2f$

Il modo più semplice di approssimare il laplaciano nel caso discreto consiste nel calcolo delle differenze delle derivate prime lungo i due assi.
Il Laplaciano si può pertanto implementare come un filtro la cui risposta impulsiva è:

$$\LARGE\underset{\text{Versione 4-vicini} }{\begin{matrix}
0 & -1 & 0 \\ -1 & 4 & -1 \\ 0 & -1 & 0
\end{matrix}}
\qquad\qquad\qquad
\underset{\text{Versione 8-vicini} }{\begin{matrix}
-2 & 1 & -2 \\ 1 & 4 & 1 \\ -2 & 1 & -2
\end{matrix}}
$$

La versione normalizzata prevedere un fattore moltiplicativo pari a 1/4 o 1/8.
**Il Laplaciano è molto sensibile al rumore, ed è incapace di rilevare la direzione del contorno.**
