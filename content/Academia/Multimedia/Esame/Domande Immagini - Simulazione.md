# Domande Simulazione:

1. Siano (0,0,'a') - (1,1, 'b') - (2,2, 'c') le terne di output dopo la codifica di una stringa mediante [[Codifica LZ77|LZ77]], qual'era la stringa originale?
	1. abbccc
	2. aabbac
	3. aababc $\textcolor{green}\surd$
	4. abacba
2. Quale affermazioni sul formato [[Bitmap|BMP]] sono vere?
	1. Si può usare per salvare img non compresse
	2. Permette l'uso di img indicizzate
	3. è proprietario
	4. Tutte vere $\textcolor{green}\surd$
3. Quale dei seguenti formati per l'archiviazione delle img può utilizzare il dithering?
	1. Nessuno
	2. PNG
	3. BMP
	4. GIF $\textcolor{green}\surd$
4. Quale delle seguente affermazioni sul [[Metodo di Canny]] è vera?
	1. In uno dei suoi passi si usa una sogliatura con isteresi
	2. I weak edge possono essere trasformati in strong edge se sono collegati o vicini
	3. In uno dei suoi passi si impiega un filtro DroG
	4. Tutte corrette $\textcolor{green}\surd$
5. In quale caso [[SSIM]] raggiunge -1?
	1. Se viene calcolata tra due img sfalsate con strisce bianche e nere alternate $\textcolor{green}\surd$
	2. Se viene calcolata tra due img con [[PSNR]] massimo
	3. Se viene calcolata tra due img con [[MSE]] minimo
	4. Se viene calcolata tra due img completemante uguali
6. Di quale parametri si tiene conto per costruire e applicare un [[filtro adattivo locale]]?
	1. Della media, ma dopo aver escluso outlier
	2. Della covarianza della matrice
	3. Nessuna corretta
	4. Della media e della varianza locale $\textcolor{green}\surd$
7. Quale tra le seguenti affermazioni sulla [[Codifica Aritmetica]] è vera?
	1. Si divide sempre il range $[0,1]$ in sotto-intervalli di dimensione uguale
	2. Il num di bit necessari è esattamente pari al doppio dell'entropia della sequenza da codificare
	3. Il codice in output è un numero decimale intero che viene poi convertito in binario
	4. Ad ogni passo si usa come codice il lower-bound di un sotto-intervallo opportunamente selezionato $\textcolor{green}\surd$
8. Quale delle seguenti affermazioni sugli operatori morfologici per immagini binarie è l'unica vera?
	1. Una [[Erosione]] seguita da una [[Dilatazione]] porta ad un'immagine uguale all'immagine di partenza
	2. Applicare la [[Chiusura]] con un elemento strutturale simmetrico è uguale a un'[[Apertura]] con elemento strutturale trasposto
	3. Una chiusura è uguale ad un'apertura con elemento strutturale di segno negativo
	4. L'apertura non ha più effetto dalla seconda applicazione in poi (compresa la seconda) $\textcolor{green}\surd$
9. Quale delle seguenti affermazioni sull'[[Elemento Strutturante|Elemento Strutturale]] è vera?
	1. Un elemento strutturale in binario può avere dei valori compresi tra zero e uno
	2. Un elemento strutturale può non essere rappresentato da una matrice
	3. Un elemento strutturale in grayscale può avere esclusivamente valori 0 o 1
	4. Nessuna vera $\textcolor{green}\surd$
10. Quale delle seguenti affermazioni sul metodo di Otsu è l'unica vera?
	1. Ad un certo passo si cerca il massimo nel vettore delle soglie locali  $\textcolor{green}\surd$
	2. Ad un certo passo si cerca il minimo nel vettore delle soglie locali
	3. Ad un certo passo si fa la media delle due soglie mediane
	4. Non viene mai considerata la varianza interclasse
