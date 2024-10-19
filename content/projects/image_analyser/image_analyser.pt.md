---
slug: analisador_de_imagens
title: Analisador de Imagens
language: pt
author: Tom
Date: 2024-10-19
---

- Status: Completo
- [_Link do projeto no GitHub_](https://github.com/tomdpb/Image-Analyser)
- Linguagem: Python

# Sobre

Em 2022 tive um problema com uns arquivos de imagem no meu computador. De alguma forma, vários arquivos foram duplicados ou até triplicados e o melhor de tudo foi que algumas das cópias eram na realidade thumbnails ou versões de menor qualidade em comparação ao arquivo original. Inicialmente comecei a abrir imagem por imagem, compará-las e deletar a imagem de pior qualidade. Isso rapidamente se tornou entediante, então tive uma ideia: e se um programa pudesse fazer isso para mim? Procurei por um programa que fizesse isso, mas não achei nada, então programei eu mesmo.

O resultado foi um programa que simplesmente chamei de Analisador de Imagens (Image Analyser), o qual está disponível na minha página do [GitHub](https://github.com/tomdpb/Image-Analyser).

# Funcionalidade

A funcionalidade do Analisador de imagens é simples. Basta dar uma pasta para checar, e o programa retornará cada arquivo idêntico ou semelhante. Há também uma opção de apagar o arquivo de menor qualidade, mas ela está desativada por padrão.

# Por Trás das Cenas

Por trás das cenas, o Analisador de Imagens cria um tipo de impressão digital para cada imagem usando um hash de imagem que é resistente ao corte, embora essa resistência não seja realmente necessária. Em seguida, essas impressões digitais/hashes são comparadas por meio da diferença de hamming entre elas. Se a diferença for zero ou estiver abaixo do limite, saberemos que encontramos uma imagem semelhante. O programa informa as imagens semelhantes ao usuário e, opcionalmente, apaga a imagem que tiver menos pixels.
