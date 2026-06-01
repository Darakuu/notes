---
tags:
  - Academia/Multimedia/Teoria_Dei_Segnali
aliases:
  - Nyquist-Shannon
---

## Nyquist Rate
In un segnale periodico e a banda limitata, il Nyquist Rate è il doppio della più alta frequenza presente nello [[Spettro di un'Onda|spettro]].
In segnali a banda non limitata, si usa un filtro passa-basso prima di campionare.

## Teorema
Per poter ricostruire fedelmente un segnale, occorre che venga rispettata la seguente condizione:

$\large f_{s} > f_{n}$

cioè la frequenza di campionamento deve essere maggiore della Nyquist Rate, dove $f_{s}$ è il numero di campioni prelevati al secondo.

>[!example]
>Un segnale con frequenza max a $400Hz$ può essere ricostruito fedelmente prendendo i campioni con una frequenza di $800Hz$, o in altre parole prendendo 800 campioni al secondo.



