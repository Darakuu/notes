---
tags:
  - Academia/GameTheory/Definitions
  - Academia/GameTheory/FiniteGame
---
## Finite Game
Se i set di strategie di ogni giocatore sono set discreti (i.e. finiti), e tutte le combinazioni delle strategie possono essere enumerate con il loro payoff.

La proprietà dell'enumerazione ci torna utile per rappresentare il gioco con una matrice multi-dimensionale.

## Table Representation

Caso: Finite Game con 2 Players.

- Players:$\ I, II$
- Strategies $I:S_{1},\dots,S_{i},\dots,S_{m}$
- Strategies $II:T_{1},\dots,T_{j},\dots,T_{n}$

| $I$ \ $II$ | $T_{1}$          | $T_{2}$        | $\dots$ | $T_{j}$        | $\dots$ | $T_{n}$        |
| ---------- | ---------------- | -------------- | ------- | -------------- | ------- | -------------- |
| $S_{1}$    | $a_{11}b_{11}$   | $a_{12}b_{12}$ |         |                |         | $a_{1n}b_{1n}$ |
| $S_{2}$    | $a_{21}b_{21}$   | $a_{22}b_{22}$ |         |                |         |                |
| $\dots$    |                  |                |         |                |         |                |
| $S_{i}$    |                  |                |         | $a_{ij}b_{ij}$ |         |                |
| $\dots$    |                  |                |         |                |         |                |
| $S_{m}$    | $$a_{m1}b_{m1}$$ |                |         |                |         | $a_{mn}b_{mn}$ |
 

- $a_{ij}=$ [[Payoff]] del [[Player]] $I$ quando vengono giocate le [[Strategy|Strategie]] $S_{i}$ e $T_{j}$
- $b_{ij}=$ [[Payoff]] del [[Player]] $II$ quando vengono giocate le [[Strategy|Strategie]] $S_{i}$ e $T_{j}$
