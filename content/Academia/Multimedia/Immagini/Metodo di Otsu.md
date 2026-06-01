---
tags:
  - Academia/Multimedia/Immagini/Segmentazione
  - Academia/Multimedia/Immagini/Segmentazione/Thresholding
---
# Metodo di Otsu

È una tecnica automatica di selezione della [[Thresholding|Threshold]] T.
Il metodo massimizza la varianza interclasse, è basato solo su operazioni effettuate sull'istogramma dell'immagine.

## Riassunto

L’algoritmo di Otsu può essere riassunto come segue:
- Calcolare l'istogramma normalizzato;
- Calcolare le somme cumulative $P_{1}(k)$ per $k=0,1,\dots,L-1$
- Calcolare le medie cumulative $m(k)$ per $k=0,1,\dots,L-1$
- Calcolare la media globale delle intensità $m_{G}$;
- Calcolare la varianza interclasse per $k=0,1,\dots,L-1$;
- Ottenere la soglia k* che massimizza la varianza interclasse
	  (se il massimo non è unico, ricavare k* come media dei valori di k corrispondenti ai vari massimi trovati)
- Ricavare la misura di separabilità $\eta^*$ per $k=k^*$

### Se c'è rumore?
In alcuni casi l’immagine presenta un livello di rumore tale da rendere complessa la segmentazione tramite sogliatura. Spesso l’applicazione di un filtro di smoothing permette di ridurre il problema.

### Se c'è illuminazione non uniforme?
Nel caso in cui l’immagine sia illuminata in maniera non uniforme o abbia delle non uniformità nella riflettanza, la segmentazione tramite thresholding può risultare piuttosto complessa. Una soluzione semplice al problema consiste nel partizionare l’immagine in rettangoli non sovrapposti e su di essi effettuare la segmentazione.

## Spiegazione Completa

todo