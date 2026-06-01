---
tags:
  - Triennale
---
# Numeri interi $\geq 1$
Si applica la divisione intera per 2 fino a ottenere 0. I resti delle divisioni, letti al contrario, formano la rappresentazione in binario puro.

![[Pasted image 20231210191533.png|512]]
Il numero in decimale è dato dal risultato della somma $b_{i-1}+\dots+b_{1}2^1+b_{0}2^0$, dove $b$ è l'i-esimo bit della rappresentazione in binario.

$$100_{2}=1\cdot2^2+0\cdot 2^1 + 0 \cdot 2^0 = 4_{10}$$

# Numeri non-interi fra $[0,1]$

Si applica la moltiplicazione per 2 fino a ottenere 1.
Ogni volta che la parte intera è 1 si sottrae 1.
Le parti intere delle moltiplicazioni, lette nell'ordine, formano la rappresentazione in binario.
![[Pasted image 20231210191936.png|512]]

## Caso particolare:

Se prima di ottenere 1, e quindi concludere la conversione, si ottiene un decimale $d$ già visto in un passo precedente, allora si può già concludere notando che la rappresentazione in binario conterrà una parte periodica. 

![[Pasted image 20231210192114.png|256]]

Il numero in decimale è dato dal risultato della somma $b_{1}2^{-1}+b_{2}2^{-2}+\dots+b_{i}2^{-i}$, dove $b$ è l'i-esimo bit della rappresentazione in binario.

# Numeri interi e non interi $\geq 0$

Si possono applicare questi due algoritmi combinandoli insieme su parte intera e frazionaria.
![[Pasted image 20231210192338.png|256]]

La rappresentazione dei numeri a virgola mobile è vincolata da una precisione limitata: [[epsilon-macchina]]
