---
tags:
  - Academia/GameTheory/FiniteGame
  - Academia/GameTheory/NonCooperativeGame
---
## Prisoner's Dilemma


> [!def] Definizione
> Due Prigionieri possono essere condannati se uno di loro confessa. Sono in celle separate e non possono comunicare.
> - Se entrambi Non Confessano: 1 anno in prigione;
> - Se 1 confessa e l'altro no: chi confessa è Libero, l'altro è condannato per 4 anni.
> - Se entrambi confessano: 3 anni in prigione

Convertiamo in:

### Forma Strategica

- Players: $I, II$
- Strategies: $\text{Non Confessare (NC), Confessare (C)}$
- $I: \text{(C,NC)} \succ \text{(NC,NC)} \succ \text{(C,C)} \succ \text{(NC,C)}$
- $II: \text{(NC,C)} \succ \text{(NC,NC)} \succ \text{(C,C)} \succ \text{(C,NC)}$
Poi convertiamo le preferenze in Payoffs, associando ogni preferenza a un payoff:
- $I: \underbrace{ \text{(C,NC)} }_{ 3 } \succ \underbrace{ \text{(NC,NC)} }_{ 2 } \succ \underbrace{ \text{(C,C)} }_{ 1 } \succ \underbrace{ \text{(NC,C)} }_{ 0 }$
- $II: \underbrace{ \text{(NC,C)} }_{ 3 } \succ \underbrace{ \text{(NC,NC)} }_{ 2 } \succ \underbrace{ \text{(C,C)} }_{ 1 } \succ \underbrace{ \text{(C,NC)} }_{ 0 }$
In forma tabella:


| $I$ \ $II$ | NC  | C   |
| ---------- | --- | --- |
| NC         | 2,2 | 0,3 |
| C          | 3,0 | 1,1 |
- $(1,1)$ è la soluzione stabile (Cioè il [[Nash Equilibrium]])

La forma generale del Prisoner's Dilemma è:


| $I\text{\\}II$ | NC    | C     |
| -------------- | ----- | ----- |
| NC             | $a,a$ | $b,c$ |
| C              | $c,b$ | $d,d$ |
con $c>a>d>b$.

