---
tags:
  - Academia/GameTheory/Definitions
  - Academia/GameTheory/Theorem
---
## Preliminari al Teorema di Nash

nota: userò set / insieme in maniera intercambiabile a seconda di come mi suona meglio.
### Power Set 

Dato un set $A$, $\mathbb{P}(A)$ è il **power set**.
Denotiamo con $2^A$ l'insieme di tutti i sottoinsiemi non vuoti di $A$.

In altre parole: $2^A=\mathbb{P}(A)\setminus \{\emptyset\}$

### Set Valued Mapping

oppure Correspondence, Multifunction, Point-To-Set Mapping

Dati $X \subseteq \mathbb{R}^n, Y \subseteq \mathbb{R}^m, X,Y \neq \emptyset$

Una **Multifunzione** (o uno qualsiasi dei sinonimi sopra) $F$ da $X$ a $Y$ assegna ad ogni elemento di $X$ un sottoinsieme di $Y$, e scriviamo:
$$
F:X \to 2^Y
$$

> [!info] Dominio di una multifunzione
> $dom(F)=\{ x \in X: F(x) \neq \emptyset \}$

![[Pasted image 20241017093132.png|256]]


> [!info] Grafico di $T:X \to 2^Y$
> $gr(F)=\{ (x,y) \in X\times Y: x \in dom(F)\ ,\ y \in F(X) \}$

Il miglior esempio di una multifunzione è una [[Best Response]].

Dato un gioco $\Gamma=(X,Y,f,g)$ la Best Response del Player $I$ è la multifunzione:

$\large BR_{I}:Y \to 2^X$ 

Il set di strategie del Player $I$ che massimizza il Payoff di $I$, supponendo che $II$ giochi la strategia $y$ è:

$BR_{I}(y) = \{ \bar{x} \in X:f(\bar{x},y) \geq f(x,y)\ \forall x \in X \}$

Viceversa, la Best Response del Player $II$, supponendo che $I$ giochi $x$, è:

$BR_{II}(x) = \{ \bar{y}  \in Y:f(x,\bar{y})\geq f(x,y)\ \forall\}y \in Y$

---

Precedentemente, abbiamo detto che un punto è un [[Nash Equilibrium]] se:

$$
\begin{align}
\text{NE}(\bar{x},\bar{y})\leftarrow X\times Y:\ & f(\bar{x},\bar{y})\geq f(x,\bar{y})\ \forall\ x\  \\
& \text{AND}  \\
& g(\bar{x},\bar{y})\geq g(\bar{x},y)\ \forall\ y
\end{align}
$$
$(\bar{x},\bar{y})$ è un Nash Equilibrium.

Scriviamo questa cosa nella seguente forma:

$\bar{x} \in BR_{I}(\bar{y})$
$\bar{y} \in BR_{II}(\bar{x})$

Essenzialmente dicono la stessa identica cosa, ma quest'ultima forma ci permette di dimostrare il teorema di Nash più facilmente.

### Aggregate Best Response Multifunction

$BR:X\times Y \to 2^{X\times Y}$
$BR:(x,y) = BR_{I}(y) \times BR_{II}(x)$

riscriviamo la cosa detta pocanzi più formalmente:

$(\bar{x},\bar{y}) \text{ è un NE} \iff (\bar{x},\bar{y}) \in BR(\bar{x},\bar{y})$
con:
- $\bar{x} \in BR_{I}(\bar{y})$
- $\bar{y} \in BR_{II}(\bar{x})$

### Punto Fisso (Fixed Point)

Consideriamo uno spazio topologico $X$

$F:X \to 2^X$, $\bar{x} \in X$ è un punto fisso per $F$ se $\bar{x} \in F(\bar{x})$

Concludiamo che un $\text{NE}$ è un punto fisso per la Multifunzione Aggregata.
Quindi l'esistenza di un Nash Equilibrium prova l'esistenza di un punto fisso per la Best Response.

> [!def] Spazio Topologico ha valori convessi

Siano $X,Y$ spazi topologici.
Uno spazio topologico $F:X \to 2^Y$ ha valori non-vuoti, chiusi, o convessi se $F(X)\   \forall\ x \in X$ è un insieme non-vuoto, chiuso o convesso

### Upper SemiContinuous (USC)



> [!def] Teorema 1
> wip

> [!def] Teorema 2
> wip

Il Teorema di Nash si basa su:

![[Kakutani Fixed Point Theorem]]

Questo teorema ci aiuta nella dimostrazione.

> [!def] Quasi-Concavità
> wip


## Teorema di Nash

### Ipotesi

### Tesi

### Dimostrazione