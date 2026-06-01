---
tags:
  - Academia/Multimedia/Immagini/Restauro
  - Academia/Multimedia/Immagini/Restauro/FiltriAdattivi
---
Le più semplici misure statistiche di una variabile casuale sono la sua media e la sua varianza.
La risposta del filtro in ogni punto $(x, y)$ su cui è centrata la regione $S_{xy}$ si basa su quattro quantità:
- $g(x,y)$: il valore dell'immagine rumorosa in $(x,y)$
- $\sigma^2_{\eta}$: la varianza del rumore che corrompe $f(x,y)$
- $m_{L}$: la media locale dei pixel in $S_{xy}$
- $\sigma^2_{L}$: la varianza locale dei pixel in $S_{xy}$

$\Large\displaystyle\hat{f}(x,y)=g(x,y)-\frac{\sigma^2_{\eta}}{\sigma^2_{L}}[g(x,y)-m_{L}]$

Si vuole che il filtro abbia il seguente comportamento:
- Se la varianza del rumore è pari a zero, vogliamo che restituisca g(x,y). Questo è il caso più banale in cui il rumore è nullo.
- Se la varianza locale è alta rispetto a quella del rumore, il filtro dovrebbe restituire un valore prossimo a g(x,y).
	- Un'alta varianza locale è associata ai bordi, che vogliamo preservare.
- Se le due varianze sono pressocché uguali, il filtro deve fornire come risposta il valore medio aritmetico dei pixel di $S_{xy}$
	- Questa condizione si presenta quando la regione locale ha le stesse proprietà della stessa immagine, e il rumore locale può essere ridotto con la media.

