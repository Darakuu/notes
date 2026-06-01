---
tags:
  - Academia/Multimedia/Immagini/Segmentazione
  - Academia/Multimedia/Immagini/Segmentazione/Thresholding
---
Sono basati sull'analisi dell'Istogramma (e quindi senza alcuna info sulla struttura dell'immagine).
I metodi di segmentazione basati sull’analisi dell’istogramma sono spesso utilizzati grazie alla loro semplicità implementativa ed efficienza computazionale.
Queste tecniche calcolano un istogramma a partire dai pixel (es. intensità) e utilizzano i sui picchi e le sue valli per localizzare i cluster dell’immagine.

Supponiamo di avere un oggetto chiaro su sfondo scuro e che il suo istogramma sia quello mostrato in figura. I pixel dell’oggetto e del background sono raggruppati in due mode dominanti.

![[Pasted image 20231211022215.png|Istogramma con due mode dominanti]]

- Scelta una soglia T che separa le due mode, un punto $(x,y)$ tale che $f(x,y)>T$ sarà un punto dell'oggetto, altrimenti sarà assegnato allo sfondo.
- Se T è una costante che può essere applicata all'intera immagine, si parla di sogliatura globale.
- Se T varia sull'immagine si parla di sogliatura variabile
- Nel caso in cui sia necessario discrimanre più di due classi, la segmentazione diventa complessa. Meglio usare altri approcci.

La buona riuscita degli algoritmi basati sugli istogrammi dipende dalla larghezza e dalla profondità delle valli che separano le mode dell’istogramma. 
I fattori che influenzano le proprietà delle valli sono:
- La separazione tra i picchi
- Il rumore presente nell'immagine
- La dim relativa dell'oggetto rispetto allo sfondo
- L'uniformità della sorgente luminosa
- L'uniformità delle proprietà di riflettanza dell'immagine

Il rumore compromette pesantemente l'istogramma, così come l'illuminazione.