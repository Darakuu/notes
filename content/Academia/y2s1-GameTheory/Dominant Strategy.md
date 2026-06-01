---
tags:
  - Academia/GameTheory/Definitions
---
## Dominant Strategy


> [!def]- Strategia Dominante
> 
Consideriamo un [[Game]] $T=(N_{}(x_{i})_{i\in N}\ ,\ (f_{i})_{i\in N})$
Per un Player $i \in N$, dati $X_{i}', X_{i}'' \in N, X_{i}'\neq X_{i}''$
diciamo che $X_{i}'$ **domina** $X_{i}''$ se:
$\large f_{i}(x'_{i},x_{-i})>f_{i}(x''_{i},x_{-i})\ \forall\  x_{-i}$
dove
$x_{-i}=(x_{1},\dots,x_{i-1},x_{+1},\dots,x_{n})$ rappresenta tutte le strategie giocate da tutti i player, escluso $x_{i}$

Dunque, $x_{i}'$ è la **strategia dominante**, ossia quella che dà a un [[Player]] il [[Payoff]] più alto, indipendentemente dalle strategie giocate dagli altri giocatori, mentre $x_{i}''$ è la **strategia dominata**.

Questa definizione suggerisce un approccio per risolvere giochi statici, individuando ed eliminando le strategie dominate: [[Iterated Elimination of Strictly Dominated Strategies|IESDS]]