---
tags:
  - Academia/Multimedia/Immagini/Restauro
  - Academia/Multimedia/Immagini/Restauro/StatisticheOrdine
---
$\Large\displaystyle\hat{f}(x,y)=\frac{1}{mn-d}\sum_{(s,t) \in S_{xy}}g_{r(s,t)}$
Supponiamo di cancellare i valori intensità $\frac{d}{2}$ più bassi e più alti di $g(s,t)$ nell'intorno $S_{xy}$, e assumiamo che i rimanenti $g_{r}(s,t)$ rappresentino i pixel del denominatore.
Un filtro formato dalla media di questi pixel viene detto filtro di media alpha-trimmed.

Se d=mn-1 $\to$ diventa un filtro [[Mediano]].
Utile per forme di rumori multiple altrimenti, ad esempio combinazioni di [[Rumore Sale & Pepe]] e [[Rumore Gaussiano]]