---
tags:
  - Academia/Multimedia/Immagini/Formati
aliases:
  - BMP
---
Utilizzato per immagini non compresse, raster, a tono continuo.

# BMPv3

È la più diffusa, permette R/W su disco veloce, occupa più spazio in quanto l'immagine è non compressa. Non supporta l'alpha.
![[Pasted image 20231210160019.png|600]]
Fino a 8bit/pixel usa una palette per rappresentare il colore. Dai 16bit/pixel, usa una terna RGB.
# BMPv4,v5

Poco diffuso come file indipendente, usato piuttosto all'interno di applicazioni come working file.
Supporta alpha e spazi di colore continui, e può incorporare immagini come JPEG o PNG.

## Struttura BMP:

- **Header del file**: info su file, viene rimosso se la bitmap è interna ad applicazione / libreria
- **Blocco di informazioni**: info su dimensioni in pixel, e gamma di colore usata.
	- **Header della BitMap**: da v4 in poi
		- \*modello di colore:
		- \*palette: Per profondità $\leq 8$, si usa palette dove ogni colore è rappresentato da RGBQuad: RGB+Byte riservato
- spazio vuoto
- **Mappa di Pixel**: Struttura dati principale, ad ogni pixel corrisponde un elemento della tavolozza, o componenti cromatiche.
- spazio vuoto: in v4, v5 serve a incorporare altre immagini.

## Ha senso comprimere?

BMP non comprime per leggere e scrivere su disco velocemente, dato che non si devono effettuare calcoli aggiuntivi per (de)comprimere.
Esiste un algoritmo per comprimere BMP utilizzando la codifica [[Codifica RLE|RLE]], ma viene comunque battuto da altri formati lossless.