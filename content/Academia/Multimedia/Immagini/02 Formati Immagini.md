---
tags:
  - Academia/Multimedia
  - Academia/Multimedia/Immagini
  - Academia/Multimedia/Immagini/Formati
---
>[!Definition] Algoritmo di Compressione
>Un algoritmo di compressione è una tecnica che elimina la ridondanza di informazione dai dati e consente un risparmio di memoria

Dal momento che differenti quantità di dati possono essere usate per rappresentare la stessa quantità di informazione le rappresentazioni che contengono informazioni irrilevanti o ripetute contengono i cosiddetti dati ridondanti.

Un codice è un sistema di simboli utilizzati per rappresentare una certa quantità di informazioni. Ad ogni "pezzo" di info / evento è assegnata una sequenza di simboli codificati: una **codeword**.
Il numero di simboli che costituisce ciascun codice è la sua lunghezza.
In immagini, si parla di correlazione, e quindi ridondanza, spaziale. Nei video è presente anche la temporale.

Spesso, i dati contengono informazioni ignorate dall'occhio $\to$ è ridondante nel senso che non viene usata.
# Formati di Immagini

>[!Definition] Formato di Immagine
>Un formato di file di un’immagine è una modalità standard per organizzare e immagazzinare i dati di un’immagine. Esso definisce come i dati vengono disposti e, se esiste, il tipo di compressione utilizzata.

>[!Definition] Standard di Compressione
>Gli Standard di Compressione di un'immagine, invece, definiscono le procedure e gli algoritmi per la compressione e decompressione, cioè per la riduzione della quantità di dati necessari per rappresentare un'immagine


## Immagini Binarie

- CCITT: Usato per FAX, telefonia etc
- JBIG1 e JBIG2, anch'esso per fax

## Immagini a Toni Continui

- JPEG 
- [[Bitmap]]: Windows BMP, usato per immagini non compresse.
- [[GIF]]: Usa codifica LZW lossless, per immagini da 1 a 8 bit.
- [[PNG]]: Comprime immagini lossless fino a 48 bit/pixel con trasparenza, codificando la diferenza tra il valore di ciascun pixel e il valore predetto in base a pixel precedenti.
- PDF
- TIFF: Tagged Image File Format, contenitore per standard di compressione

