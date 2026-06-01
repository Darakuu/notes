---
tags:
  - Academia/Multimedia
  - Academia/Multimedia/Immagini
  - Academia/Multimedia/Immagini/Segmentazione
---
# Introduzione

La segmentazione è un processo di partizionamento di un’immagine in regioni disgiunte e omogenee.
>[!definition]+ Definizione Formale
>Sia R l’intera regione spaziale occupata dall’immagine. Il processo di segmentazione può essere visto come il partizionamento di R in n sottoregioni, $R_1, R_{2},\dots, R_{n}$ tali che:
>
>$\displaystyle\bigcup^n_{i=1}R_{i}=R$
>$R_{i}$ è un insieme connesso, $i=1,2\dots,n$
>$R_{i} \cap R_{j} = \emptyset$ per tutti i valori i e j, con $i\neq j$ 
>$Q(R_{i})=$**TRUE** per $i=1,2\dots,n$
>$Q(R_{i}\cup R_{j})=$**FALSE** per ogni coppia di regioni adiacenti $R_{j},R_{i}$ 
>
>Con $Q(R_{k})$ predicato definito sui punti di un insieme $R_{k}$
>
>Ogni pixel deve appartenere a una regione, I punti appartenti a una regione devono essere 4,8-connessi.
>Le regioni devono essere disgiunte.
>I pixel appartenenti ad una regione devono soddisfare un certo predicato Q.
>Due regioni adiacenti devono essere diverse nel senso del predicato Q.


# Strategie di Segmentazione

Non esista una segmentazione generale.
Principalmente:
- Edge Based;
- Thresholding;
- Statistical Region Merging.

[[Operatore Laplaciano]].

- [[LoG]]
- [[DRoG]]

- [[Metodo di Canny]] - Edge based
- [[Thresholding]]
- [[Metodo di Otsu]]
- [[Statistical Region Merging]]