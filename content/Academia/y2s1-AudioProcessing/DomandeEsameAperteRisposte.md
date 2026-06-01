---
draft: true
---

# Domande Aperte

## Velocità del suono 

Calcolare la velocità del suono nell’aria alle seguenti temperature: 
- $( T_1 = 0^\circ C )$
- $( T_2 = 20^\circ C )$
- $( T_3 = -20^\circ C )$
- $( T_4 = 35^\circ C )$

![[Pasted image 20241130173259.png]]

![[Pasted image 20241130173307.png]]
## Bitrate

- Cos'è il bitrate nell'audio digitale? Da quali valori dipende? Cosa rappresentano tali valori?

> [!success] Risposta
> Bitrate è il termine utilizzato per descrivere la quantità di dati trasformati in audio. A un bitrate superiore corrisponde generalmente una migliore qualità dell'audio
> Bitrate è la quantità di informazioni rispetto ad un determinato intervallo di tempo.

- Discutere delle operazioni di sovracampionamento e sottocampionamento. Cosa sono? Come si possono effettuare? Che effetti hanno?

![[Pasted image 20241130173242.png]]

- Un segnale audio non compresso con bitrate pari a 1200 kbps e frequenza di campionamento pari a 44000Hz viene sottocampionato 2 volte. La prima volta il bitrate viene portato a 600 kbps e la seconda volta a 300kbps. Dopo il primo sottocampionamento il segnale non presenta distorsioni. Dopo il secondo sottocampionamento si rileva invece una distorsione. È possibile una cosa del genere? Motivare.

> [!success] Risposta
>Sì, è possibile. La presenza o meno di distorsioni dipende dal rapporto tra la **frequenza di campionamento** del segnale e la **frequenza massima del contenuto audio** (spettro del segnale).
>
>- **Primo sottocampionamento**: Riducendo il bitrate da **1200 kbps a 600 kbps**, il numero di campioni per secondo potrebbe rimanere sufficiente per rispettare il **Teorema del Campionamento di Nyquist**, secondo il quale la frequenza di campionamento deve essere almeno il doppio della frequenza massima del segnale. In questo caso, non ci sarebbero distorsioni.
>    
>- **Secondo sottocampionamento**: Quando il bitrate è ulteriormente ridotto a **300 kbps**, potrebbe verificarsi una riduzione della frequenza di campionamento al punto che questa non soddisfa più il criterio di Nyquist. Questo provoca un fenomeno noto come **aliasing**, in cui le componenti frequenziali più alte si sovrappongono alle frequenze più basse, introducendo distorsioni udibili nel segnale​.
>    
>
Quindi, è plausibile che il primo sottocampionamento non causi problemi, mentre il secondo li introduca, se la frequenza di campionamento diventa troppo bassa.

- È possibile stabilire un range di valori per la frequenza di Nyquist di tale segnale? Se sì qual è?

> [!success] Risposta
> Sì, basta evidenziare la relazione tra bitrate, frequenza di campionamento, profondità in bit e numero di canali. Quindi:
> 
> $bitrate=f_{C}\times N \times C$
> 
> Inventiamoci dei numeri, ad esempio, $N=16$ bit usati per quantizzare, e $C=2$ suono **Stereo**.
> 
> Abbiamo:
> $1200\ kbps=F_{C}\times 16\ bit \times 2$
> 
> Per formula inversa ricaviamoci la frequenza di campionamento (**NB**: $1200\ kbps = 1200000\ bps$ ):
> 
> $F_{C}=\dfrac{1200\times 1000}{16 \times 2}=37500 Hz$ - Segnale originale
> 
> $F_{C}=\dfrac{600\times 1000}{16 \times 2}=18750 Hz$ - Segnale dopo il primo sottocampionamento
> 
> $F_{C}=\dfrac{300\times 1000}{16 \times 2}=9375 Hz$ - Segnale dopo il secondo sottocampionamento
> 
> Ricordiamoci che la $F_{C}$ è il doppio di $F_{N}$ nel campionamento, quindi il range di frequenze di Nyquist per ogni campionamento è:
> - Segnale Originale: $\dfrac{37500}{2}=18750\ Hz$
> - Segnale dopo primo subsampling: $\dfrac{18750}{2}=9375\ Hz$
> - Segnale dopo secondo subsampling: $\dfrac{9375}{2} = 4687.5\ Hz$
> 
> Quindi in realtà già dal primo sottocampionamento siamo sotto i $20\ kHz$ 'safe' per non avere aliasing o distorsioni di sorta.

## Rumore

- Quando un segnale sonoro si definisce “rumore bianco”? Per cosa può essere utilizzato tale rumore? Discutere.

![[Pasted image 20241130173141.png]]

- Quale, tra i possibili tipi di rumore sonoro, viene impiegato per equalizzare un segnale per far sì che tutte le frequenze siano percepite allo stesso volume? Motivare la risposta.

![[Pasted image 20241130173132.png]]
## Varie (syllabus)

- Perché è preferibile parlare di volume “percepito”?

> [!success] Risposta
> Il volume percepito è legato alla risposta soggettiva dell’orecchio umano alle diverse frequenze e intensità sonore. 
> Non corrisponde direttamente al valore fisico dell’ampiezza o intensità sonora misurata in decibel, ma dipende da come il sistema uditivo elabora i segnali acustici. 
> 
> Questo è evidente, ad esempio, nel fenomeno delle **curve isofoniche**, che mostrano come la sensibilità dell’orecchio vari con la frequenza: servono intensità diverse per percepire la stessa "fortezza" sonora a frequenze diverse​​.

- Cosa sono le curve isofoniche? Come sono fatte?

> [!success] Risposta
> Le curve isofoniche rappresentano l’intensità sonora necessaria affinché un suono sia percepito con lo stesso livello di loudness a diverse frequenze.
> Ogni curva corrisponde a un valore specifico di phon e mostra come il nostro orecchio sia meno sensibile alle frequenze molto basse e molto alte rispetto alle frequenze medie. 
> Queste curve sono ottenute sperimentalmente e utilizzate per descrivere la soglia di udibilità e la risposta dell’orecchio umano​​.


- Cos’è il phon? Com’è legato ai decibel SPL?


> [!success] Risposta
> Il phon è un'unità di misura della loudness, che considera la percezione umana del volume sonoro, o in altre parole, un’unità di misura che descrive il **volume percepito**. Un suono a una data intensità in dB SPL (Sound Pressure Level) ha un valore di phon equivalente a 60 dB SPL per una frequenza di 1 kHz. Questo valore viene poi adattato per altre frequenze utilizzando le curve isofoniche, poiché il nostro orecchio non percepisce tutte le frequenze con la stessa intensità.


- Qual è il volume percepito in phon di un suono a frequenza 1 KHz e ampiezza 200 dB SPL?


> [!success] Risposta
> MBARE È TIPO FUORI SCALA, ASSAI. Comunque per frequenza 1000 Hz i valori di dB SPL coincidono con il Phon, quindi 200 Phon


- Ha senso operare una compressione dei dati audio eliminando le frequenze tra 1 e 5 KHz a favore delle basse e delle alte? Motivare


> [!success] Risposta
> No, non ha senso. La banda di frequenze tra **1 e 5 kHz** è cruciale per l’ascolto umano, poiché è in questa fascia che l’orecchio umano è più sensibile e dove si trovano molte delle componenti fondamentali per la comprensione del parlato e la percezione chiara di molti strumenti musicali. 
> Eliminare queste frequenze comporterebbe una significativa perdita di qualità e intelligibilità del suono. 
> Al contrario, le frequenze molto basse o molto alte possono essere parzialmente ridotte senza compromettere gravemente la percezione sonora, dato che l’orecchio umano è meno sensibile in queste bande​​.


- Cos’è il mascheramento frequenziale? Descrivere il fenomeno. 


> [!success] Risposta
> Il **mascheramento frequenziale** è un fenomeno psicoacustico per cui un suono di una certa frequenza e intensità (detto **mascheratore**) può rendere non udibile un altro suono a frequenza simile (detto **mascherato**), se quest’ultimo ha un’ampiezza insufficiente rispetto al primo. 
> Questo effetto è particolarmente pronunciato quando le frequenze del suono mascherato sono molto vicine a quelle del mascheratore. Nella pratica, questo fenomeno viene sfruttato nei sistemi di compressione audio per eliminare le componenti sonore che, comunque, non sarebbero percepite dall’orecchio umano​.


- Qual è la differenza con il mascheramento temporale?  (non è necessario descrivere dettagliatamente il fenomeno del mascheramento temporale)


> [!success] Risposta
> La principale differenza è che il **mascheramento frequenziale** si verifica tra suoni presenti contemporaneamente a frequenze vicine, mentre il **mascheramento temporale** riguarda suoni che si verificano in successione temporale. 
> Nel mascheramento temporale, un suono intenso può mascherare un suono più debole che si verifica subito prima o subito dopo di esso. Questo effetto è utilizzato, ad esempio, nei formati di compressione audio come MP3 per ridurre l’informazione relativa ai suoni che non saranno percepiti a causa del mascheramento indotto temporalmente​​.


- Perché entrambi possono essere impiegati per comprimere un segnale audio?

> [!success] Risposta
> 
>
Entrambi i fenomeni, **mascheramento frequenziale** e **mascheramento temporale**, possono essere impiegati per comprimere un segnale audio grazie alla loro capacità di ridurre l'informazione ridondante o irrilevante per la percezione umana. Ecco come:
>
>1. **Mascheramento Frequenziale**:
>
>- Nel **mascheramento frequenziale**, i suoni a frequenze vicine a quella del suono mascheratore, e con intensità inferiore, non vengono percepiti dall'orecchio umano. In un sistema di compressione audio, è quindi possibile:
 >   - **Eliminare le componenti frequenziali mascherate** dal segnale senza influire sulla percezione sonora.
 >   - Risparmiare spazio in memoria o larghezza di banda eliminando queste informazioni irrilevanti.
>
Questo principio è ampiamente sfruttato nei codec audio come **MP3** o **AAC**, dove lo spettro del segnale viene analizzato in bande critiche e le componenti mascherate vengono rimosse.
>
>2. **Mascheramento Temporale**:
>
>- Nel **mascheramento temporale**, un suono intenso può coprire suoni deboli che lo precedono o lo seguono immediatamente nel tempo. Le componenti sonore mascherate, poiché non udibili, possono essere:
>    - **Soppresse** durante l’elaborazione del segnale.
>    - **Rappresentate con una minore precisione** nella codifica.
>
>Anche questo fenomeno è sfruttato nei codec audio, dove le componenti temporali "coperte" da suoni più intensi vengono omesse o approssimate per ridurre ulteriormente i dati da memorizzare
>
>Entrambi i tipi di mascheramento permettono di **ottimizzare l'uso dello spazio dati**, mantenendo solo le informazioni essenziali per la percezione umana. 
>Ciò è alla base della compressione **lossy**, che consente una significativa riduzione della quantità di dati necessari per rappresentare un audio, garantendo al contempo una qualità percepita accettabile.

- Cos'è la **Compansion?**

> [!success] Risposta
> La **compansion** (o "companding", da _compressing_ e _expanding_) è una tecnica usata nell'elaborazione audio per migliorare la qualità del segnale o per ridurre il rumore durante la registrazione, la trasmissione o l'archiviazione. Si basa su due fasi principali: la compressione e l'espansione, che vengono applicate rispettivamente in fase di codifica e decodifica.
>
> ### Come funziona:
>
> 1. **Compressione**:
>    
>     - Prima della trasmissione o registrazione, il segnale audio viene compresso.
>     - La compressione riduce la gamma dinamica del segnale, ovvero la differenza tra i suoni più forti e quelli più deboli.
>     - In pratica, i segnali deboli vengono amplificati, mentre quelli forti vengono attenuati.
>     - Questo permette di ridurre il rapporto segnale-rumore, migliorando la qualità del segnale trasmesso o registrato.
>     
> 
> 2. **Espansione**:
>     
>     - Durante la riproduzione, il segnale viene "espanso" per ripristinare la gamma dinamica originale.
>     - I segnali deboli vengono riportati alla loro intensità iniziale, mentre quelli forti vengono reamplificati alla loro dinamica originale.
>     
> 
> ### Applicazioni:
> 
> - **Telefonia**:
>     
>     - La compansion viene usata per migliorare la qualità audio nella telefonia analogica e digitale. Ad esempio:
>         
>         - **Compander A-Law** (standard in Europa).
>         - **Compander µ-Law** (standard negli Stati Uniti e in Giappone).
>         
>     - Questi schemi riducono la quantità di dati necessaria per rappresentare un segnale audio senza sacrificare troppo la qualità percepita.
>     
> 
> ### Benefici:
> 
> - Miglioramento del rapporto segnale-rumore (SNR).
> - Riduzione degli effetti negativi del rumore durante la trasmissione o la registrazione.
> - Utilizzo più efficiente della larghezza di banda o dello spazio di archiviazione.
> 
> ### Svantaggi:
> 
> - Introduce complessità nei sistemi.
> - Errori nel processo di compressione o espansione possono portare a una perdita di qualità audio.
> - In alcuni casi, può alterare la naturalezza del segnale audio originale


