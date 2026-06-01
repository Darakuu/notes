---
tags:
  - Academia/Multimedia/Immagini/Metriche
---
Il PSNR si definisce utilizzando l'[[MSE]].
Data un'immagine priva di rumore $m*n$ a scala di grigi $I$ e una sua versione con rumore $K$, l'MSE si ridefinisce come:

$MSE=\dfrac{1}{mn}\displaystyle\sum^{m-1}_{i=0}\sum^{n-1}_{j=0}[I(i,j)-K(i,j)]^2$

Dunque, il PSNR (in deciBel) si definisce come:

$$PSNR=10*\log_{10}(\dfrac{MAX^2_{I}}{MSE}) = 20*10\log_{10}(MAX_{I}-10*\log_{10}MSE)$$
Dove $MAX_{i}$ è il valore massimo possibile dell'immagine (generalmente 255) per img a 8 bit.