---
tags:
  - Academia/Multimedia/Immagini/Restauro
  - Academia/Multimedia/Immagini/Restauro/FiltriFrequenze
---

Filtraggio che minimizza errore quadratico medio, ingloba sia la funzione di degrado che le caratteristiche statistiche del rumore, nel processo di restauro.

Il metodo considera sia le immagini che il rumore come variabili casuali e cerca di trovare un valore $\hat{f}$ dell’immagine non corrotta $f$ tale che l’errore quadratico medio tra di essi sia minimo.

$e^2=E\{(f-\hat{f})^2\}$

Dove $E\{\cdot\}$ è il valore atteso dell'argomento.

Si assume che il rumore e l'immagine non siano correlate, che uno o l'altra abbia media nulla e che i livelli di intensità nella stima siano una funzione lineare dei livelli nell'immagine degradata.