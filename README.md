# Missões Espaciais

Site feito para a Atividade 1 da disciplina Linguagem de Script para Web (ADS, 3º período).

O tema é missões espaciais. A página mostra cinco missões (Sputnik 1, Apollo 11, Voyager 1, Hubble e James Webb), uma tabela comparando as cinco e um formulário de contato.

**Site publicado:** https://soaresm-dev.github.io/missoes-espaciais/

## Como abrir

Clonar ou baixar o repositório e abrir o `index.html` no navegador. Não precisa instalar nada.

## Arquivos

- `index.html`: a página
- `style.css`: o estilo
- `img/`: as fotos das missões

## O que fiz em cada critério

- **Landmarks e article/section:** a página usa `header`, `nav`, `main`, `aside` e `footer`. Cada parte do conteúdo é uma `section` e cada missão é um `article`.
- **Hierarquia de títulos:** tem um `h1` só (o título do site), `h2` em cada seção e `h3` em cada missão, sem pular nível.
- **Imagens:** todas ficam dentro de `figure` com `figcaption`, e cada `img` tem `alt` descrevendo a foto, além de `width` e `height`.
- **Tabela:** tem `caption`, `thead`, `th` com `scope="col"` nos cabeçalhos e `scope="row"` no nome de cada missão.
- **Formulário:** cada campo tem um `label` ligado pelo `for`, e os grupos ficam em `fieldset` com `legend`. Nome e e-mail são obrigatórios (`required`) e o e-mail usa `type="email"`. O formulário ainda não envia para lugar nenhum porque o site não tem back-end.
- **Validação:** o HTML passou no validador do W3C (validator.w3.org) e o CSS no validador de CSS (jigsaw.w3.org), os dois sem erros.
- **CSS responsivo:** comecei pelo celular, com tudo numa coluna. A partir de 768px as missões ficam em duas colunas. No celular a tabela rola para o lado dentro da própria caixa.

## Imagens

Todas são da NASA, em domínio público, e baixei do Wikimedia Commons:

- Sputnik 1 (réplica): https://commons.wikimedia.org/wiki/File:Sputnik_asm.jpg
- Apollo 11: https://commons.wikimedia.org/wiki/File:Aldrin_Apollo_11_original.jpg
- Voyager: https://commons.wikimedia.org/wiki/File:Voyager_spacecraft.jpg
- Hubble: https://commons.wikimedia.org/wiki/File:HST-SM4.jpeg
- James Webb: https://commons.wikimedia.org/wiki/File:JWST_spacecraft_model_3.png

## Autor

Murilo Soares
