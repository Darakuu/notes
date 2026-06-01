---
tags:
  - Academia/Multimedia/Immagini/Codifiche
---
Codifica di input interi non negativi con distribuzioni di probabilità che decadono esponenzialmente. Più facile da calcolare rispetto a Huffman.

>[!definition]
>Dato un numero intero $n$ non negativo e un suo divisore intero positivo $m>0$, il codice di Golomb d i $n$ rispetto a $m$, denotato come $G_{m}(n)$, è la combinazione di un codice unario del quoziente $\lfloor\frac{n}{m}\rfloor$ e della rappresentazione binaria del resto n mod m

Il codice unario di un numero intero $q$ si definisce come $q$ numeri $1$ seguiti da uno $0$.

$G_{m}(n)$ si costruisce così:
1. Si forma il codice unario del quoziente $\lfloor\frac{n}{m}\rfloor$,
2. Sia $k=\lceil \log_{2}m \rceil$, $c=2^k-m$, $r=n \mod m$, e si calcola il resto $r^t$ in modo che:
$$\begin{equation}
r^t=
\begin{cases}
r \text{ troncato a } t=k-1 \text{ bit } \qquad 0\leq r<c \\ \\

r+c \text{ troncato a } t = k \qquad\qquad \text{altrimenti}
\end{cases}
\end{equation} $$
3. Si concatenano i risultati ottenuti.

>[!example]- $G_{2}(9)$
>Calcoliamo $G_{2}(9) \to n=9, m=2$
>1. Determiniamo il codice unario del quoziente $\lfloor \frac{9}{2} \rfloor = 4$, che corrisponde al codice unario 11110
>2. Sia $k=\lceil \log_{2}2 \rceil = 1, c=2^1-2=0,r=9 \mod 2 = 1 = 0001$
>   Siamo nel secondo caso, $r>c$
>   $r+c = 0001+0000=0001$
>   Tronchiamo a $t=1$ bit, $r^1=1$
>3. Concateniamo il codice unario a $r^1$
>   111101   

L'algorimo restituisce codici di lunghezza variabile non prefissi.
Inoltre, al crescere di m diminuisce la lunghezza della stringa.



