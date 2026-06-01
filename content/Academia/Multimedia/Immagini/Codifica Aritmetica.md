---
tags:
  - Academia/Multimedia/Immagini/Codifiche
---
Codici di lunghezza variabile, all'alfabeto è associata una distribuzione di probabilità.
L'intervallo iniziale è $[0,1)$, con l'upper bound escluso. (per evitare ambiguità in decodifica).
Ad ogni passo l'algoritmo ricalcola l'intervallo dei propri simboli sull'alfabeto, sulla base della distribuzione iniziale, riducendo di volta in volta la window sull'intervallo.

>[!definition]+ Algoritmo di Codifica
>INPUT: Stringa da codificare e alfabeto con distribuzione di probabilità
>1. Inizializza l'intervallo a $[0,1)$
>2. Per ogni simbolo della stringa di input
>	1. Suddividi l'intervallo corrente in $n$ sottointervalli. Ogni sottointervallo avrà un'ampiezza proporzionale alla probabilità associata a ciascun elemento nell'alfabeto iniziale.
>	2. Selezione come intervallo corrente quello corrispondente al simbolo in analisi
>3. Il lower bound dell'ultimo intervallo (convertito in binario) è il nostro output.

## Esempio Codifica

![[Pasted image 20231210210331.png]]

Il numero di bit necessari a codificare un intervallo $[a,b)$ di dimensione $s$ è $\lceil -\log_{2}s \rceil$.
La lunghezza dell'intervallo finale è uguale al prodotto delle probabilità dei singoli simboli di input.
Il numero di bit generati dalla codifica aritmentica è esattamente pari all'**entropia**, quindi:

$\lceil -\log_{2}s \rceil = \lceil -\displaystyle\sum^N_{i=1}p(a(i))\log p(a(i)) \rceil$

Quindi la codifica aritmentica è sub-ottimale.

Nel nostro esempio: $s=(0.0688-0.06752)=0.00128$, e poichè $\lceil -\log_{2}0.00128 \rceil = 10$ Abbiamo bisogno di 10 bit per la codifica.

La conversione in binario di 0.06752 è .0001000101 e usa esattamente 10 cifre.

>[!definition]+ Algoritmo di Decodifica
>INPUT: Stringa da decodificare e alfabeto con distribuzione di probabilità
>1. Inizializza intervallo a $[0,1)$
>2. Per ogni simbolo della stringa di input:
>	1. Suddividi l'intervallo corrente in $n$ sottointervalli. Ogni sottointervallo avrà un'ampiezza proporzionale alla probabilità associata a ciascun elemento nell'alfabeto iniziale.
>	2. Seleziona il simbolo corrispondente al sottointervallo nel quale ricade il valore dell'input in analisi e seleziona tale intervallo come corrente.

## Esempio Decodifica

![[Pasted image 20231210211733.png]]