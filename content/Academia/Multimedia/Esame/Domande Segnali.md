1. Cos'è un'onda periodica? Dare una definizione il più possibile formale e fare un esempio di onda periodica
	1. Risposte: [[Onda Periodica]]
2. Cosa sono frequenza, periodo e pulsazione di un'onda periodica? Da quale relazione sono legati?
	1. Risposte: [[Onda Sinusoidale]]
3. Cosa sono frequenza, lunghezza d'onda e velocità di un'onda periodica? Se sono legate da qualche relazione, quale?
	1. Risposte:
4. Cosa sono fase e ampiezza di un'onda periodica? Sono legate da qualche relazione? Se sì, quale?
	1. Risposte: Non sono legate da una relazione.
5. Cosa rappresentano i termini nell'equazione di un'onda sinusoidale?
	1. Risposte: [[Onda Sinusoidale]], tutti i termini rappresentano la $\phi$ generica
6. Cos'è l'analisi armonica di Fourier? A cosa serve? Su quale Teorema si basa? Cosa afferma il Teorema?
	1. Risposte: [[Analisi Armonica di Fourier]]
7.  Che differenza c'è tra Serie di Fourier e Trasformata di Fourier?
	1. Risposte: La Serie si usa solo su funzioni periodiche, e ha frequenze multiple della frequenza fondamentale, [[Serie di Fourier]], [[Trasformata di Fourier]]
8. La Serie di Fourier può essere usata sempre? Se no, quali sono le condizioni sotto le quali può essere utilizzata?
	1. Risposte: No: [[Condizioni di Dirichlet]], l'onda deve essere periodica
9. Cos'è l'n-sima armonica di un'onda periodica? Con quale espressione matematica si descrive? Basandosi su tale espressione, quanto vale l'ampiezza della n-esima armonica?
	1. Risposte: L'n-sima armonica è l'onda che ha n volte la frequenza fondamentale
10. Usando la Serie di Fourier si può descrivere un'onda periodica in termini di armoniche. Cos'è l'armonica fondamentale? Da cosa è caratterizzata e come è legata alle altre?
	1. Risposte: l'Armonica fondamentale è l'armonica con n=1. Nel caso della serie di fourier, tutte la altre armoniche avranno frequenza multipla alla frequenza fondamentale dell'armonica fondamentale.
11. Dimostrare che $A\cos(\omega t+\phi_{0})$ può essere scritto come $a\cos \omega t+b\sin \omega t$
	1. Risposte: Formula di addizione del seno/coseno
12. Cos'è lo spettro di un'onda? Con quali strumenti matematici si può ottenere?
	1. Risposte: Lo [[Spettro di un'Onda|spettro]] è il contributo di frequenze.
13. Quante armoniche sono necessarie per rappresentare un'onda sinusoidale? E un'onda a dente di sega?
	1. Risposte: Per un'onda sinusoidale ne basta una, per una a dente di sega infinite
14. Cosa rappresenta la simpaticissima espressione $c_{n}=\dfrac{1}{T}\int_{-\frac{T}{2}}^{\frac{T}{2}}y(t)e^{-i\omega nt}  \, dt$, e cosa sono n, T?
	1. Risposte: è la forma compatta complessa per rappresentare i coefficienti della serie di Fourier
15.  Cos'è la frequenza di campionamento?E la frequenza più alta del segnale? Come sono legate?
	1. Risposte: In un segnale a banda limitata, è il contributo della più alta frequenza osservabile nello spettro. è la frequenza più a destra, non c'entra niente l'ampiezza.
	2. Sono legate dal fatto che la frequenza di campionamento deve essere il doppio della frequenza più alta del segnale, per il teorema di Nyquist-Shannon $f_{s}>f_{n}$
16. Come si ottiene la più alta frequenza del segnale?
	1. Risposte: Con la Serie o la Trasformata di Fourier
17. Cosa recita il teor. del campionamento di [[Teorema del Campionamento di Nyquist-Shannon|Nyquist-Shannon]]? Cosa succede se non si segue?
	1. Risposte: $f_{s}>f_{n}$ , se non si segue le frequenze ripetute e specchiate si intersecano tra loro producendo artefatti di aliasing, distorsioni etc
18. Com'è fatto lo spettro di un segnale campionato? Quali operazioni sono necessarie per ricostruire il segnale originale?
	1. Risposte: Lo spettro di un segnale campionato presenta frequenze ripetute e specchiate del segnale originale. Le operazioni necessarie sono la [[Interpolazione di Whittaker-Shannon]], l'uso di un filtro passa basso prima di tutto per levare le ripetizioni, e l'uso dell'AntiTrasformata per tornare nel dominio temporale.
19. L'aliasing è una particolare forma di distorsione nei segnali digitali. Durante quale processo viene introdotta? Si può evitare o attenuare? Se sì, come?
	1. Risposte: Viene introdotta nel campionamento. Si può evitare rispettando il teorema di Nyquist-Shannon, o facendo un filtro passa basso prima di campionare nel caso di limitazioni tecniche
20. Cosa provoca l'operazione di Sottocampionamento, e sotto quali condizioni?
	1. Risposte: Crea Aliasing. Si perdono dettagli del segnale originale, perché si sovrappongono le frequenze ripetute e specchiate che si sovrappongo alle più alte del segnale originale.
21. Cos'è la precisione di quantizzazione?
	1. Risposta: è legata alla minima variazione nella grandezza originale che induce un passaggio da un livello ad un altro nel dominio quantizzato.
	   Una precisione migliore più piccoli.
22. Qual è la differenza tra quantizzazione uniforme e non?
	1. Risposte: Nella quantizzazione uniforme a intervalli di ampiezza uguale nel dominio originale corrispondono un numero uguale di livelli di quantizzazione.
	   Nella quantizzazione non uniforme questi livelli sono variabili. Precisione di quantizzazione variabile per intervallo.
23. Cos'è l'errore max di quantizzazione uniforme? Come si calcola?
	1. Risposta: $E_{max} = \frac{VFS}{2Q}$, Massimo errore che posso commettere durante la quantizzazione, ossia max differenza tra valore effettivo e quantizzato.
24. Cosa sono i livelli di quantizzazione? Quanti sono?
	1. Risposta: Nel caso di segnali digitali, il numero massimo di livelli di quantizzazione dipende dal numero di bit che decideremo da usare per rappresentare i livelli di ampiezza del segnale (Profondità in bit) $Q=2^N$
25. La quantizzazione introduce distorsione? Perché?
	1. Risposte: Sì, perché sto rappresentando dei valori continui con valori discreti. Esempio, 2.3 e 2.2 cadranno tutti nello stesso livello intero 2. Nelle immagini osserviamo color banding l'Errore è di norma deterministico
	   In generale, valori diversi ma molto vicini appariranno uguali nel dominio discreto.
26. Il campionamento introduce distorsione? Perché?
	1. Risposte: Sì see non rispetto Nyquist-Shannon, no altrimenti. Perché Aliasing
27. Cos'è il SQNR? Come si calcola?
	1. Risposte: $2^N*\sqrt{\dfrac{3}{2}}$, [[SQNR]]
28. è possibile che, tra due diversi segnali con lo stesso SQNR, uno abbia in realtà subito una maggiore distorsione rispetto all'altro?
	1. Risposta: Sì, perché SQNR dipende solo dal numero di bit. Non dà info sul segnale
29. Cos'è la formula di Whittaker Shannon?
	1. Risposta: formula di interpolazione. [[Interpolazione di Whittaker-Shannon]]
30. Cos'è l'RMS? Come si calcola? Com'è legato a SQNR?
	1. Risposte: [[RMS]], [[SQNR]]
31. Come si può ridurre l'errore di quantizzazione percepito non cambiando il numero di livelli?
	1. Risposte: [[Dithering]]
32. Cos'è il dithering? Quali problemi legati alla quantizzazione risolve?
	1. Risposte: [[Dithering]], risolve valori vicini che cadono nello stesso livello, e errore deterministico
33. Cos'è la matrice di Bayer? Come si costruisce?
	1. Risposte: [[Ordered Dithering#Matrice di Bayer|Matrice di Bayer]], ricorsivamente.
34. Perché introdurre rumore casuale attenua l'errore di quantizzazione percepito?
	1. Risposte: [[Dithering]], inganna il sistema percettivo umano.
35. Come funziona l'ordered Dithering?
	1. Risposte: [[Ordered Dithering]]
36. Come funziona il dithering basato su diffusione dell'errore?
	1. Risposte: [[Error Diffusion Dithering]]
37. Cos'è il dithering di Floyd-Steinberg? Come si applica?
	1. Risposte:[[Error Diffusion Dithering^Floyd-Steinberg]]
38. Cos'è una Trasformata discreta?
	1. Risposte: [[Trasformata Discreta]]
39. Quali sono le proprietà della Trasformata di Haar?
	1. Risposte: [[Trasformata di Haar]], possiamo rimuovere certe parti del segnale perché riguarda tutto il segnale Haar.
40. Come si costruisce la matrice di trasformazione di una trasformata partendo da uno spazio di funzioni?
	1. Risposte:
41. Perché è conveniente che la matrice di trasformazione di una trasformata sia ortogonale?
	1. Risposte: Perché ci permette di computare velocemente la trasformata e la corrispettiva antitrasformata, cioè ci permette di tornare facilmente al segnale originale
42. Come si possono ottenere gli elementi di una base di una trasformata discreta a partire dallo spazio di funzioni che la caratterizzano?
	1. Risposte: Le righe sono elementi della base.
	   in 2D devo fare prodotto riga colonna per avere $N$ elementi $N*N$
43. Quali sono le proprietà della matrice di trasformazione usata per la Trasformata di Fourier? Che vantaggi hanno?
	1. Risposte: Coniugata , Trasposta. [[Trasformata di Fourier]]
44. Cos'è la matrice di Hadamard? Come si costruisce?
	1. Risposte: [[Trasformata di Walsh#Matrice di Hadamard|Matrice di Hadamard]], seerve a costruire in pochi semplici passaggi la Matrice per la Trasformata di Walsh. Cioè una matrice ortogonale composta da soli 1, -1
45. Quale, tra le seguenti affermazioni relative a un segnale sinusoidale, è l'unica vera?
	1. Può essere definito esattamente come somma di infinite funzioni armoniche
	2. <mark style="background: #BBFABBA6;">	 Può essere definito esattamente da una e una sola funzione armonica
</mark>
	3. Non può essere in alcun modo definito come somma di funzioni armoniche
	4. Può essere definito esattamente come somma di un numero finito di funzioni armoniche
46. Quale tra le seguenti affermazioni sulla Serie di Fourier è l'unica <mark style="background: #FF5582A6;">falsa</mark>?
	1. Esiste sia una versione per segnali continui che discreti.
	2. Non può essere usata su funzioni aperiodiche
	3. <mark style="background: #BBFABBA6;"> Può essere usata solo su funzioni continue</mark>
	4. La rappresentazione di alcune funzioni tramite essa potrebbe richiedere infinite armoniche
47. Quale tra le seguenti affermazioni sull'SQNR è l'unica falsa?
	1. <mark style="background: #BBFABBA6;">Si usa per misurare la distorsione introdotta dalla quantizzazione non uniforme</mark>
	2. Rappresenta un rapporto segnale/rumore
	3. Dipende dal rapporto tra due RMS
	4. Dipende solo dal num di bit di quantizzazione usati
48. Sia S un segnale analogico campionato con $f=2000Hz$. Il segnale campionato S' presenta dell'aliasing. Quale tra le seguenti affermazioni su S è l'unica vera?
	1. S ha frequenza fondamentale nello spettro sicuramente uguale a 2000Hz
	2. <mark style="background: #BBFABBA6;">S ha frequenza max nello spettro sicuramente superiore o uguale a 1000Hz</mark>
	3. S ha una frequenza max nello spettro sicuramente inferiore a 1000Hz
	4. Nessuna delle tre
49. Quale tra le seguenti affermazioni sulla ricostruzione di un segnale continuo a partire dalla sua controparte digitale è l'unica vera?
	1. La ricostruzione può avvenire SOLO usando un filtro passa-alto nel dominio delle frequenze
	2. <mark style="background: #BBFABBA6;">La ricostruzione può avvenire usando l'interpolazione di Whittaker-Shannon</mark>
	3. La ricostruzione è sempre fedele a prescindere dalla frequenza di campionamento adottata durante la digitalizzazione
	4. Nessuna delle tre
50. Quanto vale l'RMS di un segnale costante che vale ad ogni istante K?
	1. <mark style="background: #BBFABBA6;">K</mark>
	2. K/2
	3. K*K
	4. Nessuna delle tre
51. Quale tra le seguenti affermazioni sull'armonica fondamentale di un segnale periodico S è <mark style="background: #FF5582A6;">falsa</mark>?
	1. Tutte le altre armoniche hanno frequenza multipla rispetto alla frequenza dell'armonica fondamentale
	2. <mark style="background: #BBFABBA6;">La scelta della frequenza di campionamento, nel caso della digitalizzazione, dipende esclusivamente dalla frequenza di questa armonica</mark> (no, deve essere almeno il doppio)
	3. Corrisponde all'armonica che si ottiene per $n=1$ nella formulazione della serie di fourier
	4. La sua frequenza è la stessa della frequenza del segnale S
52. Dato il segnale $y(t)$ descritto dalla funzione armonica $y(t)=2\sin(3t)$ dire quanto vale la frequenza:
	1. 3
	2. $\frac{1}{\pi}$
	3. $\dfrac{3}{2\pi}$ <mark style="background: #BBFABBA6;">this</mark>
	4. 2
53. Quale tra le seguenti affermazioni sulla trasformata di Walsh è l'unica vera?
	1. La sua matrice di trasformazione è simmetrica
	2. La sua matrice di trasformazione contiene al più quattro valori distinti
	3. La sua matrice di trasformazione può essere sempre costruita da una matrice di Hadamard
	4. <mark style="background: #BBFABBA6;">nessuna corretta</mark>
54. Quale tra le seguenti strategie di Dithering, non garantisce un risultato uguale deterministico?
	1. Error diffusion
	2. Ordered Dithering
	3. <mark style="background: #BBFABBA6;">Random Dithering</mark>
	4. Nessuna è corretta

