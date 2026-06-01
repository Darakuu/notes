---
tags:
  - Academia/GameTheory/Definitions
---
## Decision Science

Problemi con 1 solo decisore, ma più scelte.
Si esprimono le preference di un giocatore con **relazioni binarie**.

Dato un set $A$, una relazione binaria $R$ è tale che $R \subseteq A \times A$, con $a,b \in A$, scriviamo che $(a,b) \in R$.

Rappresentiamo una [[Preferenza Debole]] come:

![[Preferenza Debole]]
$a \succeq b$ significa che preferisce $a$ rispetto a $b$, o è indifferente tra $a$ e $b$.

Per chiamarla **Preferenza Debole** ci serve che la Relazione Binaria sia:
- Completa: dato $a,b \in A$, vale $a \succeq b$ o $b \succeq a$
- Transitiva: dato $a,b,c \in A$, vale: $a \succeq b \text{ AND } b \succeq c \implies a \succeq c$


Un Problema di Decisione è una coppia $(A, \succeq)$ dove $\succeq$ è una Preferenza debole.

Abbiamo anche:

- Strict Preference:
	![[Strict Preference]]

- Indifference:
![[Indifference]]
Per rappresentare la weak preference si usa una:

![[Utility Function]]