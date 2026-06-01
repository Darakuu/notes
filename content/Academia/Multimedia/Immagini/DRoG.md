---
tags:
  - Academia/Multimedia/Immagini/Segmentazione
  - Academia/Multimedia/Immagini/Segmentazione/EdgeBased
---
Un esempio molto noto di operatore di gradiente composto è la Derivata della Gaussiana (DroG), nel quale l’operazione di smoothing utilizza una funzione gaussiana.
La gaussiana è una funzione a simmetria rotazionale la cui equazione nel caso 2D continuo è la seguente:

$\displaystyle\Large h(x,y)=e^{-\dfrac{x^2+y^2}{2\sigma^2}}=e^{-\dfrac{r^2}{2\sigma^2}}$

Il valore di $\sigma$ determina l'apertura della Gaussiana che aumenta al crescere di $\sigma$.

In figura una funzione gaussiana in cui h è rappresentata, per diversi valori di σ, al variare di r, quindi in un piano passante per il suo asse di simmetria. 
![[Pasted image 20231211021025.png|256]]
Dalla risposta impulsiva è possibile ricavare i coefficienti del relativo kernel di convoluzione attraverso un opportuno campionamento della funzione continua, a partire dalla origine, che rappresenta il punto di applicazione della maschera. 

Nel caso della gaussiana il ruolo di σ è determinante nella definizione dei pesi della maschera: se l’apertura è maggiore, l’azione di filtraggio può riguardare un intorno più ampio del punto centrale. A tal fine, σ è normalmente espresso in pixel.