---
tags:
  - Academia/Multimedia/Immagini
  - Academia/Multimedia/Immagini/Morfologia
---
## Apertura
Rimozione strutturata di punte.

![[Pasted image 20231114100341.png]]

Rende più omogenei i contorni di un'oggetto, elimina piccole interruzioni e protuberanze sottili.

$A \circ B = (A \ominus B)\oplus B$

L'Apertura altro non è che un'[[Erosione]] seguita da una [[Dilatazione]] usando lo stesso [[Elemento Strutturante|Elemento Strutturale]]. L'effetto dell'apertura è di preservare il più possibile regioni di forma simile all'elemento strutturale e di eliminare quelle differenti.

È un filtro di [[Smoothing]], di cui potenza e tipologia vengono determinati dalla forma e dalle dimensioni di B.

È importante notare anche le loro [[Proprietà Apertura Chiusura|proprietà]]

>[!Example]- Esempio Apertura
>![[Pasted image 20231114094131.png]]

>[!Application]- Applicazione Apertura
>![[Pasted image 20231114095119.png]]
>Un esempio di problema che richiede l'applicazione dell'apertura è l'eliminazione di linee dall'immagine in figura. In questo caso, viene utilizzato un elemento strutturale a forma sferica di raggio pari a quello dei cerchi da preservare, che è maggiore dello spessore delle linee.

