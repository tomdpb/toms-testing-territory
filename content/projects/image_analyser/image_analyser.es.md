---
slug: analizador_de_imagenes
title: Analizador de Imágenes
language: es
author: Tom
Date: 2024-10-19
---

- Estado: Completado
- [_Enlace del proyecto en GitHub_](https://github.com/tomdpb/Image-Analyser)
- Lenguaje: Python

# Sobre el Programa

En 2022 tuve un problema con algunos archivos de imagen de mi ordenador. De alguna manera, varios archivos se habían duplicado o incluso triplicado y lo mejor era que algunas de las copias eran en realidad miniaturas o versiones de menor calidad en comparación con el archivo original. Al principio, empecé abriendo imagen por imagen, comparándolas y eliminando la de menor calidad. Esto se convirtió rápidamente en una tarea tediosa, así que se me ocurrió una idea: ¿y si un programa pudiera hacer esto por mí? Busqué un programa que lo hiciera, pero no encontré nada, así que lo programé yo mismo.
El resultado fue un programa al que llamé simplemente Analizador de Imágenes (Image Analyser), que está disponible en mi página de [GitHub](https://github.com/tomdpb/Image-Analyser).

# Funcionalidad

La funcionalidad del Analizador de Imágenes es simple. Basta con darle una carpeta para comprobar y el programa devolverá todos los archivos idénticos o similares. También existe la opción de eliminar el archivo de menor calidad, pero está desactivada automáticamente.

# Entre bastidores

Entre bastidores, el Analizador de Imágenes crea un tipo de huella digital para cada imagen utilizando un hash de imagen que es resistente al corte, aunque esta resistencia no es realmente necesaria. A continuación, estas huellas dactilares/hashes se comparan mediante la diferencia hamming entre ellas. Si la diferencia es cero o inferior al umbral, sabemos que hemos encontrado una imagen similar. El programa informa al usuario de las imágenes similares y, opcionalmente, elimina la imagen con menos píxeles.
