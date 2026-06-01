---
tags:
  - Academia/Multimedia/Immagini
---

1) Operazioni sulle immagini: 
	- Cosa sono DroG e LoG? Quali sono le loro caratteristiche? Quali sono le differenze?
	   
	- Come funzionano, in generale, gli algoritmi di segmentazione basati su thresholding? Di quali problematiche possono soffrire? Discutere.
	  
	- Perché nel primo passo del metodo di Canny si utilizza l’operatore DroG? Quali sono gli altri passi del metodo di Canny? Fornire una breve spiegazione per ognuno.
	  
	- Com’è definito l’operatore Laplaciano per una funzione f(x,y)? Scrivere un kernel per eseguire tale operazione su un’immagine. Che cosa si riesce ad individuare?
2) Operatori morfologici: 
	- Cosa si intende con morfologia matematica applicata alle immagini? Cos’è l’elemento strutturante?
	   
	- Come si può ottenere, per un’immagine binaria, un filtro di edge detection usando la morforlogia?
	   
	- Quali sono gli effetti delle operazioni di Dilatazione ed Erosione per un’immagine a scala di grigi?
	  
	- Cos’è l’elemento strutturante nella morfologia matematica applicata alle immagini?
	   
	- A cosa serve l’operatore morfologico Bottom-hat?
	   
	-  A cosa serve l’operatore morfologico Top-hat? 	  
	  
	- Nella definizione dell’operazione di Bottom-hat si utilizza l’operatore di Chiusura. Com’è definita tale operazione di Chiusura? Quali sono i suoi effetti? 
	  
	- Indicare almeno una proprietà matematica dell’operatore di Chiusura.
	  
	- Cos’è l’elemento strutturante nella morfologia matematica applicata alle immagini? 
	  
	- Nella definizione dell’operazione di Top-hat si utilizza l’operatore di Apertura. Com’è definita tale operazione di Apertura? Quali sono i suoi effetti? 
	  
	- Indicare almeno una proprietà matematica dell’operatore di Apertura. 
	   
	- Com’è definita l’operazione di Apertura in funzione di quella di Erosione e Dilatazione? 
	  
	- Riportare almeno due delle proprietà matematiche dell’operazione di Apertura? 
	  
	- Come si può ottenere un edge detector utilizzando gli operatori morfologici? 
	  
3) Rumore nelle immagini: 
	- Qual è la differenza tra il rumore casuale nelle immagini e il rumore periodico? 
	  
	- Sia P una distribuzione di probabilità gaussiana di legge P(z) con media $\bar{z}$=0 e deviazione standard σ=3, che rappresenta la probabilità che il valore di un pixel subisca uno scostamento (errore) di intensità pari a z. Scrivere l’espressione matematica della legge P(z), Calcolare la probabilità di subire uno scostamento pari a -5. 
	  
	- Questo tipo di rumore può essere attenuato? Se si, spiegare come, se no, spiegare il perché. 
	  
	- Cos’è il rumore casuale nelle immagini? Da cosa può essere introdotto? 
	  
	- Sia P una distribuzione di probabilità di legge P(x)=0.10 per x=0; P(x)=0.25 per x=255; P(x)=0 altrimenti. Dove x è un valore (intero) di luminanza a 8 bit. Come si chiama il rumore che segue tale distribuzione di probabilità? Discutere del significato della distribuzione descritta. 
	  
	- Cos’è il filtro di media contrarmonica? Com’è definito? 
	  
	- Il filtro di media contrarmonica può essere utilizzato per attenuare il suddetto rumore con distribuzione P? Se si, spiegare come. Se no, proporre un altro tipo di filtraggio. 
	  
4) Codifiche e Standard di compressione: 
	- Codificare in LZ77 la stringa "M O L O M M L M O M M M L M M" (priva di spazi) con |S|=7 e |LA|=6 - Decodificare il risultato ottenuto al passaggio precedente, esplicitando tutti i passaggi e verificando che il risultato così ottenuto combaci con la stringa iniziale.
	   
	- All'interno dello standard di compressione GIF, in cosa consiste l'applicazione dell'effetto "dithering"? Descrivere pro e contro di tale effetto? 
5) Metriche di qualità: 
	- Cos’è una metrica di qualità per le immagini? 
	  
	- Qual è la differenza tra metriche Full Reference, Reduced Reference e No Reference? 
	  
	- Qual è la differenza tra [[PSNR]] e [[SSIM]]? 
	  
	- Sia 124376 l’[[MSE]] tra due immagini a 16 bit, calcolare il PSNR.
	   
6) Canny Edge Detector: 
	- Definire i quattro passi dell’algoritmo di Canny fornendo una breve ma completa descrizione di ognuno di essi.
	  
	- Quali sono i principali punti di forza del Canny Edge Detector?

[[Domande Immagini - Simulazione]]

Digital Forensics: (_probabilmente non c'è_)
	- Cosa si intende con PRNU di un’immagine? Per cosa viene utilizzato in ambito forense? 
	- Può essere utilizzato altrettanto efficacemente per i video? Motivare la risposta. 