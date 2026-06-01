---
tags:
  - Academia/Multimedia/Immagini/Segmentazione
  - Academia/Multimedia/Immagini/Segmentazione/EdgeBased
---
# Metodo di Canny
## Introduzione

Il modello di bordo considerato è un fronte ripido monodimensionale $b(x)$ cui è aggiunto rumore Gaussiano bianco.
Si assume che l’individuazione del bordo sia realizzata tramite una convoluzione con un filtro $f(x)$ avente risposta impulsiva $h(x)$ antisimmetrica e nulla al di fuori di un intervallo $[-W,W]$

Un bordo è individuato da un massimo locale della convoluzione tra l’immagine ed il filtro. Il filtro è scelto sulla base di **tre criteri di efficacia** definiti da Canny.
## Criteri di efficacia
Il metodo di Canny si basa su tre obiettivi di base:
- Rapporto di errore basso: 
	- Tutti gli edge devono essere trovati e non esistono risposte spurie. Cioè, gli edge individuati devono essere più vicini possibile agli edge veri
- I punti di edge devono essere ben localizzati:
	- Gli edge localizzati devono essere più vicini possibile agli edge reali. Cioè, la distanza tra un punto segnato come edge e il centro del vero edge deve essere minima.
- Risposta al punto di un singolo edge:
	- L’algoritmo deve istituire solo un punto per ogni punto di edge reale. Cioè, il numero di massimi locali attorno all’edge reale dovrebbe essere minimo. 
	  Questo significa che l’individuatore non dovrebbe identificare pixel con edge multipli dove esiste solo un singolo punto di edge.

## Step del metodo di Canny:
- Step 1: Calcolo Gradiente ([[DRoG]]): magnitudo e direzione 
- Step 2: Eliminazione dei punti il cui valore del gradiente non è superiore ai valori dei vicini (interpolazione lineare) nella direzione del gradiente 
- Step 3: Sogliatura con **Isteresi** mediante 2 soglie $T_{1}$ e $T_{2}$ 
- Step 4: Edge linking per legare gli strong edge individuati con eventuali weak edge adiacenti

Anche se la complessità della formulazione impedisce la determinazione di una soluzione analitica, è possibile procedere alla ricerca del massimo con metodi numerici.

## Non-Maximum Suppression

L'immagine di risposta all'operatore, se vista come una superfice 3D, è caratterizzata da valli (valleys) e rilievi. Le curve di massimo dei rilievi, le creste, sono detti ridges. Per ottenere una risposta univoca dall'edge detector è necessario un algoritmo che sopprima tutti i responsi multipli, **ovvero i pixel che sono caratterizzati da valori alti di risposta all'operatore ma che non sono massimi locali per esso.**

La non-maximum suppression si ottiene cercando i pixel che sono di massimo per la magnitudo lungo la direzione del gradiente. Si tengono solo i ridges sopprimendo tutti gli altri punti che non sono all'altezza massima locale.

Si verifica l’esistenza di un massimo locale lungo la direzione del gradiente. Ciò richiede l’interpolazione dei pixel mancanti.
![[Pasted image 20231211021630.png|256]]

## Soglia con Isteresi

La qualità dei risultati ottenibili con il metodo di Canny, superiore a quella di tutti gli altri operatori di gradiente, si giustifica con il fatto che il metodo utilizza due soglie, una per la individuazione degli edge più netti, l’altra per l’individuazione degli edge più deboli. 
Questi ultimi sono però presi in considerazione **solo se risultano connessi ad edge netti**. 

Ruolo fondamentale nell'algoritmo di Canny gioca anche la scelta di sostituire il tradizionale approccio di sogliatura (thresholding) a soglia singola con una tecnica a doppia soglia detta **histeresys thresholding**.

La doppia sogliatura (Histeresys thresholding) viene operata dopo l'applicazione della non-maximum suppression. 
- Si fissano due soglie T1 e T2 con T1>T2; 
- Tutti i punti di valore maggiore di T1 sono di edge; 
- Tutti i punti di valore compreso fra T1 e T2 sono detti weak edges; 
- Un weak edge diventa edge solo se è contiguo ad un edge.

### Edge Linking

Individuato il punto di edge si costruisce la tangente alla curva (normale al gradiente in quel punto) e si usa questa informazione per predire il successivo punto (in questo caso r o s)

Integrando la fase di thresholding con quella di linking il metodo ne guadagna in robustezza e versatilità.

Diminuisce pertanto l’influenza del rumore, ed aumenta la probabilità di rivelare ‘veri’ edge deboli. 
In tutti i metodi di edge detection basati sul gradiente, occorre confrontare il risultato dell’operazione di derivazione in ogni punto dell’immagine con uno (o più) valori di soglia, per determinare se si tratta di un punto di edge. 
Il valore di soglia determina direttamente la sensibilità dell’edge detector. 

Per immagini **non rumorose**, la soglia può essere scelta in modo che le discontinuità di ampiezza, anche relative a zone a basso contrasto, siano interpretate come edge. Nelle immagini rumorose la **scelta** del valore di soglia è molto più critica, diventando un elemento di tradeoff tra la possibilità di rivelare falsi contorni (indotti dal rumore) e la possibilità di mancare contorni veri (relativi a piccoli dettagli).

## Impatto del parametro $\sigma$ (Gaussian Kernel Size)

La scelta di $\sigma$ impatta sulla detection dei relativi edge:
- Alti valori di $\sigma$ permettono di trovare edge a scale più grandi;
- Piccoli valori di $\sigma$ permettono di scovare dettagli più piccoli.