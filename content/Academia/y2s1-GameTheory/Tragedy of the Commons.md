---
tags:
  - Academia/GameTheory/FiniteGame
  - Academia/GameTheory/NonCooperativeGame
aliases:
  - Exploitation of a Common Resource
---
## Tragedy of the Commons

Can be formulated like a [[Prisoner's Dilemma]], but can change.

Two farmers have to graze their sheep on a common field.
They can graze:
- A lot
- A little

$P_{1}$ Preferences:
(Lot, Little) $\succ$ (Little,Little) $\succ$ (Lot,Lot) $\succ$ (Little,Lot)
$\quad\quad3\quad \succ \quad2\quad \ \succ \quad\ \ 1\quad \ \ \ \succ \quad0\quad$

$P_{2}$ is similar.

| $I \text{\\}II$ | Little | Lot   |
| --------------- | ------ | ----- |
| Little          | $2,2$  | $0,3$ |
| Lot             | $3,0$  | $1,1$ |

> [!tip] Penalità
> Introduciamo una penalità per cambiare il gioco e costringere i players a cooperare.

| $I \text{\\}II$ | NB                     | B                      |
| --------------- | ---------------------- | ---------------------- |
| NB              | $2,2$                  | $\textcolor{red}{3,0}$ |
| B               | $\textcolor{red}{0,3}$ | $1,1$                  |
$2,2$ Diventa il nuovo valore migliore!
