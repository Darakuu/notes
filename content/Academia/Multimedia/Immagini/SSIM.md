---
tags:
  - Academia/Multimedia/Immagini/Metriche
---
# Structural SIMilarity

È un indice restituito da una funzione che misura la similarità tra due immagini. Poiché l'occhio umano è in grado di estrarre informazioni strutturali, la perdita di informazioni strutturali può essere usata per approssimare la distorsioni di un'immagine. Ha valori compresi tra \[-1,1].

Misura la similarità tra due immagini (**Full Reference**).
Si basa sul fatto che il sistema visivo umano è in grado di estrarre info strutturali dal campo visivo.

Pertanto, una misurazione della perdita di info strutturale può fornire una buona approssimazione alla distorsione percepita.
Sono quindi considerate le info strutturali in un'immagine come quegli attributi che riflettono la struttura degli oggetti sulla scena, <mark style="background: #FA6767A4;">indipendenti da luminanza e contrasto medio</mark>.

Si considerino $x$ , $y$ due segnali non negativi corrispondenti rispettivamente all'immagine campione e a quella distorta. dati $\mu_{x}$, $\mu_{y}$, $\sigma^2_{x}$, $\sigma^2_{y}$, $\sigma_{xy}$ (covarianza tra $x$ e $y$), si definisce:

>[!definition] Formula SSIM
$SSIM(x,y)= \dfrac{(2\mu_{x}\mu_{y}+C_{1})(2\sigma_{xy}+C_{2})}{(\mu_{x}^2+\mu_{y}^2+C_{1})(\sigma^2_{x}+\sigma^2_{y}+C_{2})}$

Le due costanti $C_{1}$ e $C_{2}$ servono per i casi limite (evitare la divisione per 0) e sono definite come:

$C_{1}=(K_{1}L)^2$
$C_{2}=(K_{2}L)^2$

con $L=255$ per immagini a 8 bit, e $K_{1},K_{2}\ll 1$ costanti molto piccole.

>[!important]+ Valore -1, 1
>- Il valore $1$ si ottiene quando le due immagini sono **IDENTICHE**
>- Il valore $-1$ si ottiene quando ci sono elementi **TOTALMENTE DIFFERENTI**, ad esempio se si hanno bande alternate di spessore 1. E c'è relazione con la dimensione dell'immagine.
>![[Pasted image 20231209221739.png|250]]



