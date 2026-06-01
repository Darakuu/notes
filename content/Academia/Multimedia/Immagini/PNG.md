---
tags:
  - Academia/Multimedia/Immagini/Formati
---
# Portable Network Graphics

Usato per immagini compresse lossless, raster, a tono continuo. Sviluppato per sostituire [[GIF]].

## Colore

Supporta immagini truecolor (RGB) da 24 a 48 bit per pixel, e il canale alpha per la trasparenza: 32 bit per pixel, RGB-A.
Supporta immagini grayscale fino a 16 bit per pixel.
NON supporta spazi di colore diversi da RGB.
Come per BMP, i pixel dell'immagine possono contenere un puntatore a una palette, oppure le coordinate grayscale/rgb (+alpha eventualmente).

## Struttura

1. Header
	- 8 Byte, contiene metadati
2. Chunks:
	- **Ausiliari**: contengono info secondarie come valori gamma dell'immagine, background-color, etc...
	- **Critici**:
		- Header: info su immagine (dim, canali, colori)
		- Palette: se si usa indexing
		- Dati: contiene ulteriori chunk critici a cascata
		- Marker di fine immagine

## Pre-Compressione

Prima fase della compressione: usa filtraggio predittivo.

- Il filtro predice il valore di ciascun pixel basandosi sui valori dei pixel vicini, e memorizza la differenza tra il valore predetto e quello effettivo.
- Se l'immagine non è molto fotorealistica (e quindi c'è molta ridondanza), tramite il filtraggio predittivo può diventare più comprimibile.
Salvo dunque una matrice degli errori:

![[Pasted image 20231210191010.png|512]]

## Compressione: algoritmo Deflate

È un algoritmo di compressione lossless, una variante di LZW.
Opera su dati di dimensione massima di 64KB, e può utilizzare la codifica di Huffman per ridurre ulteriormente la dimensione dei dati.
Anche qui si può usare interlacing, con una migliore qualità rispetto a [[GIF]]
