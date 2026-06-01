---
tags:
  - Academia/Algoritmi
  - Academia/Algoritmi/SecondaProva
  - Academia/Algoritmi/RetiDiFlusso
---
# Grafi e Reti di Flusso

Con il termine **Rete** indichiamo un grafo pesato, cioè un grafo ai cui nodi e/o archi sono associati valori numerici detti **pesi**. In generale, in una rete gli archi sono interpretabili come canali attraverso cui fluiscono dei beni, rappresentabili come grandezze discrete o continue, possono rappresentare dei valori assoluti o valori relativi (i.e. per unità di tempo). 

In questo contesto, i pesi degli archi rappresentano delle capacità e dei costi, mentre i pesi sui nodi possono rappresentare la quantità di beni che entrano o escono in quei nodi.


> [!def] Rete di Flusso
> Una rete di flusso è definita come un grafo orientato $G=(V,E)$ **senza cappi** e tale che:
> - Ad ogni arco $(u,v) \in E$ è associato un valore non negativo, $c(u,v)\geq 0$ detto **capacità** dell'arco. Se l'arco $(u,v)$ non è presente in $E$ allora assumiamo che esso abbia capacità nulla, cioè $c(u,v)=0$
> - Nella rete di flusso ci sono due vertici speciali: il vertice **sorgente**, indicato con il simbolo $s$, ed il vertice **pozzo** (o destinazione), indicato con il simbolo $t$. I rimanenti vertici sono detti **vertici di transizione**.
> - Ogni vertice giace su qualche cammino dalla sorgente al pozzo. Il grafo è quindi connesso e pertanto vale $|E|\geq|V|-1$


> [!example]- Rete di Flusso
> ![[Pasted image 20240901193638.png]]


## Flusso Reale di una Rete

Data una rete $G=(V,E)$ con capacità $c:V \times V\to \mathbb{R}_{0}^+$


> [!def] Flusso Reale
> Un Flusso Reale in $G$ è una funzione $\phi:V \times V \to \mathbb{R}_{0}^+$ che soddisfa le seguenti proprietà:
> - **Vincolo di Capacità**: $\forall (u,v) \in V\times V$, si richiede che $\phi(u,v)\leq c(u,v)$
> - **Conservazione del flusso ( Kirchoff's Law )**:  $\forall\ u \in V - \{s,t\}$, si richiede che:
>   
>   $\displaystyle\sum_{v\in V}\phi(u,v)=\displaystyle\sum_{v \in V}\phi(v,u)$
>   
>   Cioè che il flusso uscente da $u$ deve essere uguale a quello entrante in $u, \forall u \in V - \set{s,t}$

La quantità $\phi(u,v)$ è detta **Flusso Reale** lungo l'arco $(u,v)$.


### Valore del flusso reale

Il valore $|\phi|$ di un flusso reale $\phi:V\times V\to \mathbb{R}_{0}^+$ è dato da:

$$
|\phi |= \displaystyle\sum_{v \in V} \phi(s,v) - \displaystyle\sum_{v \in V}\phi(v,s)
$$
(= flusso Netto uscente da $s$)

### Esempio

Ad ogni arco $(u,v) \in E$ sono associato due valori, $x/y$, con $x=\phi(u,v)$ e $y = c(u,v)$.
Inoltre, entrambi i vincoli sono rispettati.

![[Pasted image 20240901203903.png|360]]

## Flusso Netto di una Rete

Data una rete $G=(V,E)$ con capacità $c:E\to \mathbb{R}_{0}^+$ e con un flusso reale $\phi:V\times V\to \mathbb{R}_{0}^+$ poniamo:


> [!def] Flusso Netto
> $f_{\phi}(u,v)=\phi(u,v)-\phi(v,u)$
> $\forall (u,v) \in V\times V$ 

La quantità $f_{\phi}(u,v)$ è detta **flusso netto** dal vertice $u$ al vertice $v$ **indotto** dal flusso reale $\phi$

## Proprietà

Dati:
- $G=(V,E)$ una rete di flusso,
- $c:V\times V\to \mathbb{R}_{0}^+$ la sua capacità,
- $f_{\phi}:V\times V\to \mathbb{R}$ il suo flusso (netto) indotto,
- $\phi:V\times V\to \mathbb{R}_{0}^+$ il suo flusso reale;

Allora valgono le seguenti proprietà:


> [!info] Proprietà Flusso Netto
> - **Vincolo di Capacità**:
>   $f_{\phi}(u,v) \leq c(u,v) \quad \forall\ u,v \in V$
> - **AntiSimmetria**:
>   $f_{\phi}(u,v) = -f_{\phi}(v,u) \quad \forall\ u,v, \in V$
> - **Conservazione del Flusso**:
>   $\displaystyle\sum_{v \in V} f_{\phi}= 0 \qquad\qquad \forall\ u \in V - \{ s,t \}$

### Vincolo di Capacità

$\text{Per tutti gli } u,v \in V, \qquad f_{\phi}(u,v)\leq c(u,v)$

Il vincolo di capacità asserisce semplicemente che il flusso netto da un vertice ad un altro non può eccedere la corrispondente capacità.


$\textcolor{red}{Dimostrazione:}$
$f_{\phi}(u,v)=\phi(u,v)-\phi(v,u)\leq \phi(u,v)\leq c(u,v)$

### Antisimmetria

$\text{Per tutti gli } u,v \in V\qquad f_{\phi}(u,v) = -f_{\phi}(v,u)$

L'antisimmetria asserisce che il flusso netto da un vertice $u$ ad un vertice $v$ è l'opposto del flusso netto nella direzione inversa. 

Quindi il flusso netto da un vertice a se stesso deve essere 0, perché per ogni $u \in V$ abbiamo:

$f_{\phi}(u,v) = -f_{\phi}(u,u) \implies f_{\phi}(u,u)=0$


$\textcolor{red}{Dimostrazione:}$
$f_{\phi}(u,v)=\phi(u,v)-\phi(v,u)$
$f_{\phi}(v,u)=\phi(v,u)-\phi(u,v)$
$-f_{\phi}(v,u)=\phi(u,v)-\phi(v,u)=f_{\phi}(u,v)$
$\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_$
$f_{\phi}(u,v)=-f_{\phi}(u,u)=0$

### Conservazione del Flusso

$\text{Per tutti gli } u \in V - \{ s,t \}, \qquad \displaystyle\sum_{v \in V}f_{\phi}(u,v) = 0$

La proprietà di conservazione del flusso asserisce che il flusso totale uscente da un vertice di transizione deve essere **nullo**. 
Per la proprietà di antisimmetria possiamo riscrivere la proprietà di conservazione nella forma:

$\displaystyle\sum_{v\in V}f_{\phi}(v,u)=0$

cioè il flusso totale entrante in un vertice di transizione deve essere nullo.

$\textcolor{red}{Dimostrazione:}$
$$
\begin{align}
\displaystyle\sum_{v\in V}f_{\phi}(u,v) & =  \displaystyle\sum_{v\in V}(\phi(u,v)-\phi(v,u)) \\
& =\displaystyle\sum_{v\in V} \phi(u,v) - \displaystyle\sum_{v \in V}\phi(v,u)  \\
& = 0
\end{align}
$$
### Proprietà (Flusso Reale che Induce Flusso Netto)

Sia $G=(V,E,c,s,t)$ una rete di flusso con:
- capacità $c$
- sorgente $s$
- pozzo $t$

E sia $g:V\times V\to \mathbb{R}$ una funzione che soddisfi:
- Vincolo di Capacità;
- Proprietà di Antisimmetria; 
- La legge di Conservazione del Flusso (relativamente a $s,t$), 
 
Allora la funzione: $\phi_{g}:V\times V\to \mathbb{R}_{0}^+$ definita da:
$$
\phi_{g}(u,v)= \begin{cases}
g(u,v) & \text{se } g(u,v)>0 \\
 0 & altrimenti
\end{cases}
$$
è un **Flusso Reale** in $G=(V,E,c,s,t)$ che **induce il flusso netto** $g$, cioè $\Large g=f_{\phi_{g}}$

Un flusso netto può essere indotto da più flussi reali.

#### Vincolo di Capacità per $\phi_{g}:$

$$
\phi_{g}(u,v)=\begin{cases}
g(u,v) \leq c(u,v) & \text{se } g(u,v) > 0 \\
0 \qquad\ \leq c(u,v) & \text{se } g(u,v) \leq 0
\end{cases}
$$
E quindi in ogni caso: $\phi_{g}(u,v) \leq c(u,v)$


> [!tldr] Proprietà (\*)
> $(\forall\ u,v \in V)\quad \phi_{g}(u,v)-\phi_{g}(v,u)=g(u,v)$
> 
> Infatti:
> 
> $$
> \begin{align}
> \phi_{g}(u,v)-\phi_{g}(v,u)=\begin{cases}
> g(u,v)-0 & =g(u,v) &\quad g(u,v) > 0  \\
> 0 - 0 & = g(u,v) &\quad g(u,v) = 0 \\
> 0 - g(v,u) & = - g(v,u) = g(u,v) &\quad g(v,u)<0 \\
> 
> \end{cases}
> \end{align}
> $$
> 

#### Conservazione del flusso per $\phi_{g}:$

Sia $u \in V - \{ s,t \}$

$$
\begin{align}
\displaystyle\sum_{v\in V}\phi_{g}(u,v)-\displaystyle\sum_{v\in V}\phi(v,u) & = \displaystyle\sum(\phi_{g}(u,v)-\phi(v,u)) \\
& = \displaystyle\sum_{v \in V}(g(u,v)) \\
& = 0
\end{align}
$$
$\Large g = f_{\phi_{g}}$, cioè $g$ è uguale al flusso netto indotto da $\phi_{g}$

Per la proprietà (\*):

$\Large f_{\phi_{g}}=\phi_{g}(u,v) - \phi_{g}(v,u) = g(u,v)$

 Pertanto $g$ è uguale al flusso netto indotto da $\phi_{g}$
### Valore del flusso netto

## Problema del Flusso Massimo

## Reti con Sorgenti e Pozzi multipli

![[Notazione di Sommatoria Implicita]]

# Metodo di Ford-Fulkerson

## Capacità Residua

## Cammini aumentanti

## Procedura di Ford-Fulkerson

## Analisi di Ford-Fulkerson

# Tagli in reti di flusso

# Teorema del Massimo Flusso / Minimo Taglio

# Algoritmo di Edmonds-Karp

# Further Reading

[[Edge Connectivity]]