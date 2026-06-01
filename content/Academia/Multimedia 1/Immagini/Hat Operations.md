---
tags:
  - Academia/Multimedia/Immagini/Morfologia
---
Una delle applicazioni principali di queste trasformazioni è la rimozione degli oggetti da un’immagine attraverso un elemento strutturante che non si abbina agli elementi da rimuovere; la loro differenza porta ad avere un’immagine in cui rimangono solo le componenti rimosse.
# Top Hat
La trasformazione top-hat si usa per oggetti **chiari** su uno sfondo **scuro** (white top-hat).
Viene spesso utilizzata per correggere efficacemente gli effetti di un’illuminazione non uniforme (shading correction).

$T_{\text{hat}}(f)=f-(f \circ b)$ 

Usa [[Apertura]].
# Bottom Hat

La trasformazione bottom-hat si usa per oggetti **scuri** su uno sfondo **chiaro** (black top-hat).
Viene spesso utilizzata per correggere efficacemente gli effetti di un’illuminazione non uniforme (shading correction)

$B_{\text{hat}}(f)=(f \cdot b) - f$ 

![[Pasted image 20231211030836.png|384]]