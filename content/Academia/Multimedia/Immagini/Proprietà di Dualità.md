---
tags:
  - Academia/Multimedia/Immagini
  - Academia/Multimedia/Immagini/Morfologia
aliases:
  - duale
  - dualità
  - duali
---
- Erosione e dilatazione sono operazioni duali l'una dall'altra rispetto al complementare e la riflessione di un'insieme:
- $(A \ominus B)^C = A^C \oplus \hat{B}$
- $(A \oplus B)^C = A^C \ominus \hat{B}$
Quando l'[[Elemento Strutturante]] è simmetrico rispetto all'origine, come si verifica spesso, il ribaltamento di B è proprio B stesso.
Quindi, possiamo ottenere l'erosione di un'immagine attraverso B semplicemente dilatando il suo sfondo (cioè dilatando $A^c$) con lo stesso elemento strutturante e complementando il risultato.

>[!info]- Immagine e Sfondo
>Sia $A$ un'immagine rappresentata sotto forma di matrice e $A^c$ la sua complementare, allora $A^c$ rappresenta lo sfondo dell'immagine A.

>[!Dimostrazione della Dualità]-
>$$
\begin{flalign}
(A \ominus B)^c =\\ \{ z|(B)_{z} \subseteq A \}^c =\\= \{ z|(B)_{z} \cap A^c = \emptyset \}^c =\\= \{z|(B)_{z} \cap A^c \neq \emptyset  \} =\\= A^c \oplus \hat{B} && 
\end{flalign}
$$
