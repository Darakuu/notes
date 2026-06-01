---
tags:
  - Academia/Multimedia/Immagini/Formati
---
# Graphics Interchange Format

Utilizzato per immagini compresse lossless, raster, a tono continuo.
Ogni GIF ha una palette di 256 colori, 8 bit, scegliendo comunque da 16 Milioni di colori.

## Metodi di Compressione

GIF usa l'algoritmo di compressione [[Codifica LZW|LZW]] al posto della codifica RLE. Questo perché invece di codificare ogni singolo simbolo, codifichiamo coppie o terne frequenti.
È possibile interlacciare le linee dell'immagine per fornire un'anteprima a dimensione ridotta (utile per il web), cioè memorizzare una riga sì, e l'altra no.

### Fasi di Compressione:
1. Encoder
	1. Crea flusso di dati GIF a partire da dati raster
	2. Include info necessarie per riprodurre gli elementi grafici
	3. Ottimizza la memorizzazione dell'info (rimuovi ridondanza) (aggiungi [[Dithering]])
2. Decoder
	1. Processa flusso di dati GIF
3. Conformità: controlla se versione di Encoder e Decoder coincidono.

## Colore

Basato su una palette VGA a 256 Colori:
- Ogni entry occupa un Byte,
- Le entry sono un sottoinsieme dei 16 Milioni di colori possibili tra terne RGB complete ($256\cdot256\cdot256$)
- Si può ottimizzare la scelta dei 256 colori per migliorare la qualità dell'immagine compressa. (ad esempio, col [[k-means]], il colore è indicato dal centroide perfetto)
Ad ogni pixel dell'immagine corrisponde un indice nella palette. (si potrebbe usare reindexing).

## Dithering

L'immagine compressa potrebbe presentare delle zone di color banding, si può applicare il dithering, che però abbassa la comprimibilità dell'immagine (in quanto riduce la ridondanza).
Palette ottimizzata con reindexing + Dithering: miglior risultato.

## Trasparenza

Una entry della palette può essere definita come 'trasparente': assume il colore dello sfondo $\to$ NON è un canale alpha, è un abuso di un canale di colori, tipo chroma key.

## Animazione

Dalla v89a è possibile inserire animazioni nelle immagini: frame che si alternano secondo un delay pre-impostato. Ogni frame ha la sua **Graphics Control Extension (GCE)** per gestire questo delay.
Di default la ripetizione non avviene.

Nella GIF animata, la Global Color Table cambia, e usa una Local Color Table se i frame sono molto diversi tra loro.
