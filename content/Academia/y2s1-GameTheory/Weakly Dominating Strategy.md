---
tags:
  - Academia/GameTheory/Definitions
---
## Weakly Dominating Strategy


> [!def] Weakly Dominating Strategy
> Dato il gioco $\Gamma=(N,(X_{i})_{i\in N},(f_{i})_{i\in N})$,
> Per un player $i \in N$, sia $x_{i}',x_{i}'' \in X_{i},$ con $(x_{i}'\neq x_{i}'')$,
> $x_{i}'$ Weakly Dominates (WD) $x_{i}''$ se:
> $\Large f(x_{i}',x_{-i})\geq f_{i}(x_{i}'',x_{-i})\ \forall\ x_{-i}$
> AND:
> $\Large f_{i}(x'_{i},x_{-i})>f_{i}(x''_{i},x_{-i})\ \forall\  x_{-i}$, per qualche $x_{-i}$


La definizione dice che $x_{i}'$ non è peggiore di $x_{i}''$, **e** in qualche caso è strettamente migliore. La possiamo vedere come un rilassamento della [[Dominant Strategy]]


> [!success] Esempio
> ![[L03_2024-10-08.jpg]]
> Le operazioni:
> - A: $2 = 2$;
> - B: $1 > 0$
> Significano che $I$:
> - è indifferente tra A o B se $II$ gioca C,
> - mentre preferisce A se $II$ gioca D
> E quindi A è una **Weakly Dominant** Strategy.


Possiamo costruire quindi [[Iterated Elimination of Weakly Dominated Strategies|IEWDS]]




