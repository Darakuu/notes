---
tags:
  - Academia/Multimedia/Teoria_Dei_Segnali
---

La Trasformata è un'operazione matematica che ci permette di passare da uno spazio di funzioni a un altro.
Nel caso di spazi vettoriali, la trasformata corrisponde ad un cambio di base.
I segnali digitali si possono vedere come elementi di uno spazio vettoriale, pertanto possono essere rappresentate come combinazioni lineari di una base dello spazio. Tipicamente si usa la [[Base Canonica]] per rappresentare i segnali digitali.

## Perché usare una Trasformata?

L'Operazione di Trasformata nel caso discreto ci permette di utilizzare un'altra base, fornendoci strumenti per il calcolo dei nuovi coefficienti.

A seconda della trasformata utilizzata, la nuova matrice dei coefficienti che otteniamo potrebbe godere di alcune proprietà caratteristiche della trasformata utilizzata, che rendono più semplice il trattamento delle immagini per certe operazioni (e.g. compressione, enhancement, detection)

## Cosa caratterizza una Trasformata?

1. **Lo spazio di funzioni a cui vogliamo passare:** rappresenta il cuore della trasformata e consiste nell'insieme di funzioni elementari attraverso cui descrivere la funzione originale. Tutte le proprietà utili dipendono da questo spazio.
2. **Complessità di computazione**: Bisogna tenere conto del carico computazione, per questo cerchiamo come proprietà la **ortogonalità** delle funzioni elementari.

## Quante e quali Trasformate?

Sono teoricamente infinite, in Multimedia vediamo nel dettaglio:
- [[Trasformata di Haar]]
- [[Trasformata di Walsh]]
- [[Trasformata di Fourier]]