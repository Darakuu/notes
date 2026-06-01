---
tags:
  - Academia/GameTheory/Definitions
---
## Strategic Game

Uno strategic game si definisce come:

$\Large \Gamma=(N,X_{1},\dots,X_{n},f_1,\dots,f_{n})$

e consiste di:
- Set di [[Player]] N, con $|N|=n$;
- Set di [[Strategy|Strategie]] $X_{i}$, per ogni player $i \in N$
- Set di [[Strategy Profile|Strategy Profiles]] $X_{n}$
- [[Payoff Function]] $f_{1}: X\to \mathbb{R}, \forall i \in N$
	- Rappresenta cosa il player $i$ ottiene quando viene giocato un dato strategy profile $x$

## Lists of Elements for a Game:

- Set of Players $N$,
- Set of Outcomes $O$,
- funzione $h:X\to O$,
- [[Preferenza Debole]] 
- [[Utility Function]] $u:O\to \mathbb{R}, \quad \forall i \in N$ (for each player)

Per semplificare, introduciamo come detto pocanzi la [[Payoff Function]], in relazione alla utility.

$f_{i}(X) = u_{i}(h(x))$