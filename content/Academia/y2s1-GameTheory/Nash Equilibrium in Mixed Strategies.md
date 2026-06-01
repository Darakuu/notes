---
tags:
  - Academia/GameTheory/Definitions
---

Iniziamo con un esempio:


> [!success] Testa / Croce (Matching Pennies)


Due giocatori lanciano due monete, se entrambe le monete escono testa, o entrambe croce, vince il Player $I$ (e vince 1€), altrimenti, se escono diverse, vince il Player $II$.


![[Pasted image 20241021202937.png|200]]

Non c'è un [[Nash Equilibrium]] puro, perché non c'è dominanza.

Aggiungiamo quindi delle probabilità (stocastiche) alle strategie. Assumiamo che:
- $I$ giochi $H$ con probabilità $p$ e $T$ con probabilità $1-p$;
- $II$ giochi $H$ con probabilità $q$ e $T$ con probabilità $1-q$.

![[Pasted image 20241021203110.png|240]]

Adesso computiamo i payoff del Player $I$ quando gioca la strategia $(p,1-p)$ in risposta alla strategia $(q,1-q)$ del Player $II$:

$f(p,q)=1 \cdot pq - 1 \cdot p(1-q) - 1 \cdot q(1-p) + (1-p)(1-q)$

Abbiamo moltiplicato i coefficienti della tabella pura con quelli della tabella di probabilità miste. 
Continuiamo:

$$
\begin{align} \\
f(p,q) & = pq-p+pq-q+pq+1-q-p+pq \\
& = pq-2p-2q+1 \\
& = 2p(2q-1) -2q+1

\end{align}
$$

Vogliamo che tutto sia espresso in funzione di $p$ per semplificarci dei calcoli
