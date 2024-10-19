---
slug: bildanalysator
title: Bildanalysator
language: de
author: Tom
Date: 2024-10-19
---

- Status: Vollständig
- [_GitHub Projekt Link_](https://github.com/tomdpb/Image-Analyser)
- Sprache: Python

# Über

Im Jahr 2022 hatte ich ein Problem mit einigen Bilddateien auf meinem Computer. Irgendwie waren mehrere Dateien doppelt oder dreifach vorhanden, und das Beste daran war, dass es sich bei einigen der Duplikate um Miniaturansichten oder eine viel schlechtere Version des Originals handelte. Zunächst ging ich jedes Bild einzeln durch, verglich es und wählte das Bild mit der besseren Qualität. Das war lästig, und so kam ich auf eine Idee: Was wäre, wenn ein Programm das für mich tun könnte? Ich suchte, fand aber nichts, also beschloss ich, es selbst zu programmieren.
Das Ergebnis ist ein Programm, das ich einfach Bildanalysator (Image Analyser) gennant habe und das auf meinem [GitHub](https://github.com/tomdpb/Image-Analyser) verfügbar ist.

# Funktionsweise

Die Funktionsweise des Bildanalysator ist einfach. Geben Sie einfach ein Verzeichnis an, in dem er suchen soll, und er gibt alle Dateinamen zurück, von denen er annimmt, dass sie identisch oder ähnlich sind. Es gibt auch die Möglichkeit, das Löschen kleinerer Dateien zu aktivieren, aber das ist standardmäßig deaktiviert.

# Hinter den Kulissen

Hinter den Kulissen erstellt der Bildanalysator für jedes Bild eine Art Fingerabdruck unter Verwendung eines Bild-Hashes, der resistent gegen Beschneidung ist, obwohl diese Resistenz nicht wirklich erforderlich ist. Diese Fingerabdrücke/Hashes werden dann verglichen, indem die Hamming-Differenz zwischen ihnen ermittelt wird. Wenn die Differenz gleich Null ist oder unter dem Schwellenwert liegt, dann wissen wir, dass wir ein ähnliches Bild gefunden haben. Das Programm meldet dem Benutzer dann ähnliche Bilder und löscht optional das Bild, das weniger Pixel hat.
