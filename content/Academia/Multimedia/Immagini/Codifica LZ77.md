---
tags:
  - Academia/Multimedia/Immagini/Codifiche
aliases:
  - LZ77
---
L'algoritmo opera su un'unico vettore, su cui scorre una window formata da:
- **Search Buffer**: parte già codificata
- **Lookahead Buffer**: parte da codificare

>[!important]
>L'algoritmo cerca il più lungo prefisso del lookahead presente nella finestra a partire dal search buffer

La finestra scorre ad ogni iterazione.

## LZ77 - Sliding Window

Se la ricerca va a buon fine, l'algoritmo restituisce una tripla $(D,L,<s>)$:
- $D$ = distanza o offset tra parola nel lookahead e quella nel search buffer
- $L$ = lunghezza del prefisso trovato
- $<s>$ = simbolo che compare nel lookahead buffer dopo il prefisso
Altrimenti, ritorna $(0,0<s>)$
$W$=dimensione della window, Search + Lookahead

![[Pasted image 20231210212623.png|512]]


>[!example]- Esempio Codifica
>![[Pasted image 20231210212646.png]]

>[!example]- Esempio Decodifica
>![[Pasted image 20231210212851.png]]

Decodifica in short: Vai indietro di D caratteri, scrivi L caratteri, aggiungi \<s> (se $D\geq L$)