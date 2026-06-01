---
tags:
  - Academia/Multimedia/Immagini/Codifiche
---
È un algoritmo per la compressione lossless, derivato da LZ78, a sua volta un'evoluzione di [[Codifica LZ77|LZ77]].
Assegna delle codeword a lunghezza fissa a sequenze di simboli a lunghezza variabile.

>[!important] Caratteristica chiave!!!
>Una caratteristica chiave di LZW è che non necessita di una conoscenza a priori della probabilità di occorrenza dei simboli che devono essere codificate

Integrata in numerosi formati per l'imagine, tra cui [[GIF]].

LZW ha un dizionario esplicito che viene costruito dinamicamente in fase di codifica e decodifica.

Fasi dell'algoritmo:
1. Inizializza il dizionario con tutte le stringhe di len=1,
2. Trova la più lunga stringa W nel dizionario che matcha con l'input corrente,
3. Ritorna *dictionary(W)* al posto di W,
4. Salva W+carattere successivo della stringa di input nel dizionario,
5. Torna a passo 2

>[!example]- Esempio Stanco, Esempio Libro
>![[Pasted image 20231210213916.png]],
>![[Pasted image 20231210214019.png]]




