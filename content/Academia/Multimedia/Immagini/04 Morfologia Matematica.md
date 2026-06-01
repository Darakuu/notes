---
tags:
  - Academia/Multimedia/Immagini
  - Academia/Multimedia/Immagini/Morfologia
  - Academia/Multimedia
aliases:
  - Morfologia
---
In Image Processing, la **morfologia matematica** è lo studio della struttura geometrica dell'immagine.
È uno strumento matematico utile per la rappresentazione della forma di una regione: permette di ricavare i contorni, lo scheletro, etc... estraendo le sue componenti fondamentali.
Ci interessano anche tecniche morfologiche per realizzare pre- o post- elaborazioni come il filtraggio morfologico, il [[Thinning|thinning]], o la riduzione.
Inizialmente definito su immagini binarie, e facilmente estendibili a immagini a scale di grigio.

### Processamento ed Analisi della forma di una regione

La percezione visiva richiede di trasformare le immagini in modo da rendere esplicita l'informazione sulle forme delle regioni presenti in essa.

Il nostro **obiettivo** è di _Distinguere le info significative sulla forma da quelle irrilevanti._
Perciò, realizziamo degli operatori di forma che soddisfano le proprietà richieste.


### Definizioni preliminari
Gli insiemi nella morfologia matematica rappresentano degli oggietti in un'immagine:
- Immagini binarie: Oggetto definito in $\mathbb{Z}^2$ ,l'elemento dell'insieme corrisponde solo alle coordinate $(x,y)$ del pixel. Il valore è $0 = white$, oppure $1 = black$.
- Immagini grayscale: Oggetto definito in $\mathbb{Z}^3$, l'elemtno dell'insieme corrisponde alle coordinate $(x,y)$ del pixel e al suo valore di intensità.
- Il Linguaggio della morfologia matematica fa parte della Teoria degli Insiemi.

Se un elemento di $A$ è definito come $a=(a_{1},a_{2})$ valgono le [[Definizioni Insiemistiche|definizioni insiemistiche di base]].

Introduciamo a questo punto le operazioni atomiche dal quale dipendono tutte le altre operazioni:
- [[Riflessione]]
- [[Traslazione]]

L'immagine viene sondata tramite un piccolo insieme user-defined: l'[[Elemento Strutturante|Elemento Strutturale]]

Tramite l'Elemento Strutturale si implementano i due operatori primitivi dai quali derivano tutti gli altri:
- [[Dilatazione]]
- [[Erosione]]
Che a loro volta implementano:
- [[Apertura]]
- [[Chiusura]]

```start-multi-column
ID: callout_application_openclose
Number of Columns: 2
Largest Column: standard
```
![[Pasted image 20231114100838.png|Esempio Applicazione|256]]

--- column-end ---
- in (b) si noti l'eliminazione del ponte tra le due sezioni principali dovuta alla maggiore ampiezza rispetto al piccolo diametro dell'elemento strutturale. (non è contenuto interamente nell'insieme)
- Idem per le due protuberanze a destra dell'oggetto: gli elementi sporgenti sono stati eliminati.
- in (e) si noti che gli angoli che puntano all'esterno appaiono smussati, a differenza di quelli interni
-  da (f) fino a (i) notiamo che gli angoli interni sono stati arrotondati, mentregli angoli esterni sono stati immutati. 
  L'intrusione più a sinistra sul bordo di A è stata ridotta di molto nelle dimensioni a causa dell'elemento strutturale.



--- end-multi-column


A partire da queste, implementiamo le operazioni composte della Morfologia Matematica, per immagini binarie:
- [[Hit or Miss|Hit or Miss Transform]]
- [[Estrazioni dei Contorni|Estrazione dei Contorni]]
- [[Thinning|Thinning]]
- [[Thickening|Thickening]]
- [[Skeletonization|Skeletonization]]
- [[Bridge|Bridge]]
- [[Clean|Clean]]
- [[Shrink|Shrink]]
- [[Pixel FIlling|Pixel FIlling]]
- [[Region Filling|Region Filling]]
- [[Connected Components|Connected Components]]
- [[Convex Hull|Convex Hull]]
- [[Hat Operations#Top Hat|Top Hat]]
- [[Hat Operations#Bottom Hat|Bottom Hat]]
Che si possono anche estendere alle immagini [[Multimedia/Immagini/Estensioni a immagini grayscale|Grayscale]]:
- [[Dilatazione#Dilatazione Grayscale|Dilatazione]]
- [[Erosione#Erosione Grayscale|Erosione]]
