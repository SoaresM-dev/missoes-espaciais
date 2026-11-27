# Missões Espaciais

Atividades 1 e 2 da disciplina Linguagem de Script para Web.

Site sobre cinco missões espaciais: Sputnik 1, Apollo 11, Voyager 1, Hubble e James Webb. Tem um resumo de cada missão com foto, uma tabela comparando elas e um formulário de contato.

Na Atividade 2 separei o site em quatro páginas (início, missões, linha do tempo e contato) e fiz a parte de SEO. O que mudou e o Lighthouse antes e depois estão no [SEO.md](SEO.md).

Link do site: https://soaresm-dev.github.io/missoes-espaciais/

## Como ver

É só entrar no link acima. Para abrir no computador, abre a pasta no VS Code e usa o Live Server, porque os links para o início apontam para `./` e abrindo o arquivo direto eles mostram a pasta em vez da página.

## O que usei

- header, nav, main, aside e footer para separar as partes da página
- section em cada parte do conteúdo e article em cada missão
- um h1 só, h2 nas seções e h3 nas missões
- figure e figcaption nas imagens, com alt, width e height
- tabela com caption, thead e th com scope
- formulário com label em todos os campos e fieldset com legend
- media query no CSS para ficar com uma coluna no celular e duas no computador

Passei o HTML e o CSS no validador do W3C e não deu erro.

O formulário ainda não envia nada porque o site não tem back-end.

## Imagens

As fotos são da NASA (domínio público) e peguei no Wikimedia Commons:

- https://commons.wikimedia.org/wiki/File:Sputnik_asm.jpg
- https://commons.wikimedia.org/wiki/File:Aldrin_Apollo_11_original.jpg
- https://commons.wikimedia.org/wiki/File:Voyager_spacecraft.jpg
- https://commons.wikimedia.org/wiki/File:HST-SM4.jpeg
- https://commons.wikimedia.org/wiki/File:JWST_spacecraft_model_3.png

Murilo Soares
