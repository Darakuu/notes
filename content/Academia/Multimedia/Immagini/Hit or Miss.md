---
tags:
  - Academia/Multimedia/Immagini
  - Academia/Multimedia/Immagini/Morfologia
---

## Hit or Miss Transform

Dato D sottoinsieme di W:

![[Pasted image 20231114104621.png]]

$\Large A \circledast B = (A \ominus B) \cap [A^c \ominus (W-D)]$

Dove $(W-D)$ è il background, quindi si può ridefinire l'operatore come:

$A \circledast B = (A \ominus B_{1}) - (A \oplus \hat{B}_{2})$

Dove $B_{1}$ è l'insieme formato dagli elementi di B associati a un oggetto, e $B_{2}$ è il background

>[!Application] Uso
>È usato come rivelatore dettagliato di una forma all'interno di una immagine. 