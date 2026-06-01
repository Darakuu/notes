---
tags:
  - Academia/Multimedia
  - Academia/Multimedia/Immagini
  - Academia/Multimedia/Immagini/Watermarking
---
# Introduzione

Gli [[02 Formati Immagini#Formati di Immagini|Standard di Compressione]] permettono la distribuzione di immagini su Internet o altri supporti. Le immagini così distribuite possono essere facilmente ricopiate, violando i diritti di proprietà.
Un modo per far fronte alla duplicazione illegale è quello di mimetizzare uno o più item di informazione, chiamati 'watermark', nell'immagine, in modo da rendere i due impossibili da separare.

## Usi

- Identificazione del copyright
- Identificazione del proprietario
- Determinazione autenticità
- Monitoraggio automatico
- Protezione per la copia

![[Pasted image 20231210221138.png|384]]

# Caratteristiche

### Resistenza agli attacchi

- Fragile/Semifragile: le modifiche al documento corrompono facilmente il watermark
- Robusto: garantisce la proprietà del documento.

### Visibilità

- Visibile: il watermark è chiaramente presente: è una sottoimmagine opaca o semitrasparente sovrapposta all'immagine originale, secondo una certa $\alpha$
	  La formula usata è $f_{w}=(1-\alpha)f+\alpha w$ 
- Invisibile: il documento marcato risulta indistinguibile dall'originale.
	  La formula usata è $f_{w}=4\left( \dfrac{f}{4} \right)+\dfrac{w}{64}$
	  (è molto debole, una compressione lo rompe.)
	  Nella formula, il /4 è la shift a sinistra per azzerare i bit più a destra, il x4 serve a shiftare di due bit nuovamente a sinistra, e il /64 mi serve per assicurarmi che siano i LSB, dove poi infilo $w$, il watermark.

>[!example]- Esempio
>![[Pasted image 20231210222241.png|512]]

### Rilevabilità

- Cieco: non devo vedere il documento originale per rilevare il watermark
- Non cieco: devo vedere il documento originale
### Riconoscibilità

- Privato: devo conoscere il watermark e possedere il documento originale
- Pubblico: il watermark è riconoscibile pur avendo scarsa conoscenza del contenuto o non avendo il documento originale.

Il watermark può essere aggiunto sia nel dominio spaziale, che nel dominio delle frequenze.

### Attacchi ai watermark 

- Compressione lossy JPEG, 
- Modifiche geometriche (rotazioni, ritagli), 
- Filtri ed effetti grafici,
- Aggiunta di rumore pseudocasuale di tipo statistico.
# Steganografia

Letteralmente scrittura nascosta: tecniche per nascondere uno scambio di info. Si possono nascondere immagini nei piani di bit meno significativi