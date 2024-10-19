---
slug: analizzatore_di_immagini
title: Analizzatore di Immagini
language: it
author: Tom
Date: 2024-10-19
---

- Stato: Completator
- [_Link del progetto su GitHub_](https://github.com/tomdpb/Image-Analyser)
- Linguaggio: Python

# Informazioni sul programma

Nel 2022 ho avuto un problema con alcuni file immagine sul mio computer. In qualche modo, diversi file erano stati duplicati o addirittura triplicati e il bello era che alcune delle copie erano in realtà miniature o versioni di qualità inferiore rispetto al file originale. All'inizio ho iniziato aprendo immagine per immagine, analizzandole ed eliminando quella di qualità inferiore. Questo è diventato presto un compito noioso, così mi è venuta un'idea: e se un programma potesse fare questo per me? Ho cercato un programma in grado di farlo, ma non ho trovato nulla, così l'ho programmato da solo.

Il risultato è stato un programma che ho chiamato semplicemente Analizzatore di Imagini (Image Analyser), disponibile sulla mia pagina [GitHub](https://github.com/tomdpb/Image-Analyser).

# Funzionalità

Il funzionamento dell'Analizzatore di Immagini è semplice. È sufficiente indicare una cartella da controllare e il programma restituirà tutti i file identici o simili. Esiste anche un'opzione per eliminare il file di qualità più bassa, ma è disattivata per impostazione predefinita.

# Dietro le quinte

Dietro le quinte, Analizzatore di Immagini crea un tipo di impronta digitale per ogni immagine utilizzando un hash dell'immagine che è resistente al taglio, anche se questa resistenza non è realmente necessaria. Queste impronte digitali/hash vengono poi confrontate utilizzando la differenza di Hamming tra di esse. Se la differenza è pari a zero o inferiore alla soglia, sappiamo di aver trovato un'immagine simile. Il programma informa l'utente delle immagini simili e, facoltativamente, elimina l'immagine con il minor numero di pixel.
