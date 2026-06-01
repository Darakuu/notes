---
tags:
  - Academia/Multimedia/Teoria_Dei_Segnali
---
Segnale di rumore che viene introdotto per ridurre gli effetti negativi legati alla [[Quantizzazione]].

Problemi che risolve: #todo

Il dithering permette di percepire continuità anche in presenza di un numero molto limitato di segnali discreti

# Random Dithering
bla
# Ordered Dithering
bla
## Matrice di Bayer
 Si definisce ricorsivamente per dimensioni che sono potenze di 2:
$$
\begin{flalign} 
M_{2}= 
\begin{bmatrix}
0 & 2 \\ 3 & 1
\end{bmatrix}
\end{flalign}
$$
La generica matrice ricorsiva invece:

$$M_{2n} = \begin{bmatrix}
4M_{n} & 4M_{n}+2 \\ 4M_{n}+3 & 4M_{n}+1
\end{bmatrix}$$
bla
# Error Diffusion

## Matrice di Floyd-Steinberg