---
tags:
  - Academia/GameTheory/FiniteGame
  - Academia/GameTheory/NonCooperativeGame
---
## Arms Race

[[Prisoner's Dilemma]]-like

Two countries need to decide wether to have a nuke arsenal or not.

Strategies: Bomb or No Bomb.

$P_{1}$ Preferences:
(B, NB) $\succ$ (NB,NB) $\succ$ (B,B) $\succ$ (NB,B)
$\quad\quad3\quad \succ \quad2\quad \ \succ \quad\ \ 1\quad \ \ \ \succ \quad0\quad$

$P_{2}$ Preferences:
(NB, B) $\succ$ (NB,NB) $\succ$ (B,B) $\succ$ (B,NB)
$\quad\quad3\quad \succ \quad2\quad \ \succ \quad\ \ 1\quad \ \ \ \succ \quad0\quad$

| $I \text{\\}II$ | NB    | B     |
| --------------- | ----- | ----- |
| NB              | $2,2$ | $0,3$ |
| B               | $3,0$ | $1,1$ |
1,1 is the solution given by [[Iterated Elimination of Strictly Dominated Strategies|IESDS]].