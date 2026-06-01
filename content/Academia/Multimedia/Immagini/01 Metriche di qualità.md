---
tags:
  - Academia/Multimedia
  - Academia/Multimedia/Immagini
  - Academia/Multimedia/Immagini/Metriche
---
# Introduzione

Una metrica di qualità è un metodo che permette di dare una valutazione **oggettiva** di un'immagine.

## Qualità Assoluta

È un dato oggettivo: completamente descritto dall'immagine e caratterizzabile mediante un insieme di attributi dell'imagine, alcuni semplici, altri composti.
Per esempio:
- Il contenuto informativo dell'immagine, cioè i soggetti e il contesto raffigurati (non matematicamente rappresentabile).
- La luminosità.
- Il colore, con i suoi sottoattributi: saturazione, naturalezza, omogeneità, scolorimento.
- Contrasto, rappresentativo del rapporto chiaro/scuro e di contorni e dettagli.
- Nitidezza (sharpness), costituita dallo sfocamento (blur) delle immagini, e dal *detail* e *contour* rendering.
- Naturalezza dei contenuti, come rettilinearità delle linee rette e curvilineità delle linee circolari, l'uniformità delle forme.
- Distorsioni spaziali o temporali, come il rumore.

## Qualità Percepita

È un parametro soggettivo, dipendente oltre che dalle caratteristiche dell'immagine, anche da altri fattori:
- L'elaborazione effettuata sull'immagine, che potrebbe alterare la nostra percezione della stessa.
- Le caratteristiche tecniche del display che sta visualizzando l'immagine
- Come il nostro sistema visivo percepisce l'immagine

Le Metriche di qualità si distinguono in [[Metriche Soggettive]] e [[Metriche Oggettive]]

## Classificazione delle metriche

Le metriche di qualità possono poi essere classificate in base alla disponibilità del segnale di riferimento, con il quale confrontare l'immagine distorta.
- **Full Reference**: Possediamo l'immagine di riferimento e quindi può essere effettuato un confronto completo.
- **No Reference**: Non si ha alcuna informazione sull'immagine di riferimento. Ci interessa particolarmente gestire questo tipo di situazioni, in quanto è la più comune.
- **Reduced Reference**: L'immagine di riferimento non è disponibile per intero, ma possiamo estrarre dall'immagine originale alcune informazioni parziali (metadati, movimento della telecamera, etc)
## Metriche Oggettive più comuni

- [[MSE]] (Mean Square Error): serve a stimare l'errore medio quadratico tra due immagini, più l'indice è basso, minore è la differenza tra le due immagini
  
- [[PSNR]] (Peak Signal to Noise Ratio), parametro per misurare la qualità di un'immagine compressa rispetto all'originale, dipende dalla differenza tra l'immagine codificata e l'originale. Maggiore è il suo valore, maggiore sarà la somiglianza con l'originale.
  
- $\nabla E^*_{a,b}CIELAB$, Si basa sulla differenza percepita tra colori nello spazio L\*a\*b\*
  
- [[SSIM]]: è un indice restituito da una funzione che misura la similarità tra due immagini. Poiché l'occhio umano è in grado di estrarre informazioni strutturali, la perdita di informazioni strutturali può essere usata per approssimare la distorsioni di un'immagine. Ha valori compresi tra \[-1,1].

I metodi tradizionali come PSNR e MSE hanno dimostrato di essere in contrasto con la percezione umana. Dato che l'SSIM interpreta la degradazione come cambiamento delle informazioni strutturali, si avvicina di più al modus operandi dell'occhio umano.
Il concetto di informazione strutturale nasce dall'idea che i pixel hanno forti inter-dipendenze, specie se spazialmente vicini.
Queste dipendenze portano con se importanti informazioni sulla natura degli oggetti nella scena.

## Metriche Soggettive più comuni

- [[SSCQE|SSCQE]]: Single Stimulus Continuous Quality Evaluation,
- [[DSCQS|DSCQS]]: Double Stimulus Continuous Quality Evaluation,
- [[MOS|MOS]]: Mean Opinion Score



