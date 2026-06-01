---
tags:
  - Academia/Multimedia/Immagini/Restauro
  - Academia/Multimedia/Immagini
  - Academia/Multimedia
---
# Introduzione
Rende migliore una immagine cercando di ripristinare il contenuto informativo/visuale. È un processo **oggettivo**, a differenza dell'enhancement, che è soggettivo.
Il restauro tenta di riparare un'immagine degradata facendo uso di una conoscenza a priori del fenomeno che ha provocato il degrado.

Ad esempio, la rimozione del *blur* è considerata una tecnica di restauro, in quanto possiamo sapere (o stimare) la funzione usata per sfocare l'immagine.
![[Pasted image 20231123155810.png|512]]

$g(x, y) = h(x, y) \star f(x, y) + \eta(x,y)$
$G(u, v) = H(u, v)F(u, v) + N(u, v)$

Dove $\star$ è la convoluzione.

Il rumore può essere sulla luminanza o la crominanza

- Rumore luminanza: L’immagine appare granulosa se osservata su uno schermo,
- Rumore crominanza: appare una sorta di patina di pixel blu o rossi, nelle zone in ombra dell'immagine

# Principali Fonti di Rumore

Si presentano durante il processo di acquisizione o trasmissione. Ad esempio, dark currents nei sensori, la sensibilità del sensore stesso, la temperatura del sensore, la compressione JPEG o lunghi tempi di posa.

# Principali Categorie di Rumore

## Rumori Casuali:

- [[Rumore Gaussiano]] 
- [[Rumore di Rayleigh]]
- [[Rumore di Erlang-Gamma]]
- [[Rumore Esponenziale]]
- [[Rumore Uniforme]]
- [[Rumore Sale & Pepe]]
Assumiamo che il rumore sia indipendente dalle coordinate spaziali e che non sia correlato all’immagine stessa (cioè, non c’è legame tra i valori dei pixel e i valori delle componenti del rumore).

## Rumori Periodici:

- [[Rumore Uniforme Periodico]]
- [[Rumore non Uniforme Periodico]]
È una distorsione sistematica, cioè che si ripete all’interno dell’immagine

## Tecniche di Restauro

Quando l’unico degrado presente in una immagine è il rumore si ha uno schema semplificato del problema:

$g(x,y)=f(x,y)+\eta(x,y)$

$G(u,v)=F(u,v)+N(u,v)$

Il Filtraggio Spaziale è il metodo migliore in situazioni in cui è presente solo del rumore additivo casuale.

## Tipi di Filtraggio Spaziale

### Filtri di Media

- [[Media Aritmetica]]
- [[Media Geometrica]]
- [[Media Armonica]]
- [[Media Controarmonica]]

In generale, i filtri di media aritmetica e geometrica si adattano meglio a trattare il rumore casuale come quello gaussiano o uniforme.
Il filtro di media controarmonica è indicato per il rumore impulsivo, o sale e pepe, ma ha lo svantaggio che deve esserne nota la tipologia (scuro o chiaro) per sceglierne di conseguenza il segno di Q.
Una scelta di segno sbagliato per Q può portare a effetti disastrosi.

### Statistiche d'Ordine

- [[Max]]
- [[Min]]
- [[Mediano]]
- [[Punto Medio]]
- [[Alpha Trimmed]]

Sono filtri spaziali la cui risposta si basa sull'ordinamento (posizione) dei valori dei pixel contenuti nell'area dell'immagine inglobata dal filtro.
La posizione relative determina la risposta del filtro.

>[!important]
>**TUTTI** i filtri visti finora vengono applicati su una immagine, senza tener conto di come
> le caratteristiche dell’immagine varino da un punto ad un altro.
### Filtri Adattivi

Il comportamento di questi filtri è guidato dalle caratteristiche statistiche dell'immagine all'interno della regione del filtro definita da una finestra rettangolare $S_{xy}$ di dimensioni $m\cdot n$:
- [[Locale Adattivo]]
- [[Mediano Adattivo]]

I filtri adattivi hanno una resa migliore rispetto ai filtri di media o di ordine, ma sono più complessi

## Tipi di Filtraggio nelle Frequenze

- [[Ideal Band Reject]]
- [[Guassiano Band Reject]]
- [[Butterworth Band Reject]]
- [[Notch Filter]]
## Stima della Funzione di Degrado

[[Filtraggio Inverso]]
[[Filtro di Wiener]]