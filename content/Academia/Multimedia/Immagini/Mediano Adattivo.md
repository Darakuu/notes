---
tags:
  - Academia/Multimedia/Immagini/Restauro
  - Academia/Multimedia/Immagini/Restauro/FiltriAdattivi
---
>[!definition]- Definizioni Preliminari
Consideriamo le seguenti definizioni:
$Z_{min}$ = valore minimo di intensita in $S_{xy}$
$Z_{max}$ = valore massimo di intensità in $S_{xy}$
$Z_{med}$ = valore mediano in $S_{xy}$
$Z_{xy}$ = valore di intensità alle coordinate $(x, y)$
$S_{max}$ = dimensioni massime ammesse di $S_{xy}$

L'algoritmo di filtraggio mediano adattivo lavora in due fasi, dette fase A e fase B, come segue:

$$
\begin{flalign}
\text{Fase A}: \quad A_{1}= z_{med}-z_{min} \\
\quad A_{2}= z_{med}-z_{max}\\ 
\quad \text{Se } A_{1}>0 \text{ AND } A_{2}<0,\text{passare alla fase B}\\ \text{Altrimenti, aumentare le dimensioni della finestra}\\

\text{Fase B:} todo\\
\end{flalign}


$$

La chiave per comprendere i meccanismi di questo algoritmo è tenere a mente che ha tre scopi principali:

1. Rimuove il [[Rumore Sale & Pepe]],
2. Ridurre altre tipologie di rumore che NON POSSONO essere a impulsi
3. Ridurre la distorsione, come assottigliamento / ispessimento eccessivo dei bordi degli oggetti.

I valori $Z_{min}$ e $Z_{max}$ sono dei valori statistici trattati come se fossero componenti del rumore a impulsi, anche se essi non sono i valori estremi (più alti e più bassi) dei pixel dell'immagine.