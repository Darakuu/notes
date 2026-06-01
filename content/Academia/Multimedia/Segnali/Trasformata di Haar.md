---
tags:
  - Academia/Multimedia/Teoria_Dei_Segnali
---
$H^T$ è la [[Matrice Trasposta]].
S è il segnale originale.
H è la matrice composta dai $H_{i}$ vettori ottenuti dalle [[Funzioni di Haar]].
**Trasformata**:
- 1D: $A = H * S$
- 2D: $A = H * S * H^T$
**AntiTrasformata**:
- 1D: $S = H^T * A$
- 2D: $S = H^T * A * H$

Vogliamo che la matrice H sia [[Ortogonalità di una Matrice|ortogonale]], che per H è vero se moltiplichiamo per il fattore di scala $\dfrac{1}{\sqrt{ N }}$.
Se l'ortogonalità è soddisfatta risulta molto semplice tornare al segnale originale.
## Proprietà:
- Ogni coefficiente della trasformata di Haar si riferisce ad aree limitate del segnale originale
- Significa dunque che eliminare un coefficiente ci fa perdere informazioni relative a quella particolare area interessata.
- Possiamo sfruttare questa proprietà per eliminare informazioni che non ci interessano (e.g. compressione) oppure per individuare elementi presenti solo in certe aree.
- Questa è la base dell'algoritmo [[Algoritmo Viola-Jones|Viola-Jones]]