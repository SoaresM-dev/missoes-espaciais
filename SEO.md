# SEO do site Missões Espaciais

Atividade 2 de Linguagem de Script para Web. O site é o mesmo da Atividade 1, mas agora tem quatro páginas e a parte de SEO.

Site: https://soaresm-dev.github.io/missoes-espaciais/

## Páginas e URLs

Antes era tudo numa página só. Separei em quatro:

- Início: https://soaresm-dev.github.io/missoes-espaciais/
- Missões: https://soaresm-dev.github.io/missoes-espaciais/missoes.html
- Linha do tempo: https://soaresm-dev.github.io/missoes-espaciais/linha-do-tempo.html
- Contato: https://soaresm-dev.github.io/missoes-espaciais/contato.html

Os nomes dos arquivos são em minúsculo, com hífen e sem acento, para a URL ficar fácil de ler.

## title, description e canonical

Cada página tem o próprio title e a própria description. Deixei o title com até uns 60 caracteres e a description entre 130 e 155, porque é mais ou menos o que aparece no Google antes de cortar.

O canonical tem o endereço completo da página. Na página inicial usei o endereço que termina em barra em vez do index.html. Os links para o início também apontam para `./`, para a mesma página não ficar com duas URLs.

## Open Graph e favicon

Todas as páginas têm og:title, og:description, og:url, og:image, og:type e og:locale. A imagem de compartilhamento (`og-imagem.jpg`) é a foto do Hubble cortada em 1200x630, que é o tamanho que o Facebook e o WhatsApp usam.

O favicon é um SVG de um planeta com anel. Também tem um PNG de 32x32 para navegador que não aceita SVG e o apple-touch-icon de 180x180 para o iPhone. Antes não tinha favicon, então o navegador procurava o favicon.ico na raiz do github.io, dava erro 404 no console e o Lighthouse tirava ponto em boas práticas.

## JSON-LD

- Início: `WebSite`
- Missões: `Article` (com as cinco fotos, o autor e as datas) e `BreadcrumbList`
- Linha do tempo e Contato: `BreadcrumbList`

O `BreadcrumbList` é igual à trilha que aparece em cima do título nas páginas internas (Início > Missões).

Passei as quatro páginas no validador do schema.org (https://validator.schema.org) e deu 0 erros e 0 avisos em todas.

## robots.txt e sitemap.xml

O robots.txt libera o site todo e diz onde está o sitemap. O sitemap.xml tem as quatro páginas com a data da última alteração.

Uma coisa que descobri fazendo: como o site fica numa subpasta (soaresm-dev.github.io/missoes-espaciais/), o Google só lê o robots.txt da raiz do domínio, que seria soaresm-dev.github.io/robots.txt. O meu fica no repositório, mas para o sitemap ser usado mesmo teria que mandar ele pelo Google Search Console.

## Imagens

- Troquei os JPG e o PNG por WebP e diminuí para 800 px de largura, que já é maior do que o card mostra. As cinco fotos juntas foram de 998 KB para 217 KB.
- Os arquivos ganharam nomes que dizem o que é a foto, por exemplo `jwst.png` virou `telescopio-james-webb.webp`.
- Todas continuam com alt, width e height. O width e o height servem para a página não pular enquanto a foto carrega.
- As três últimas fotos têm `loading="lazy"`. As duas primeiras não, porque já aparecem quando a página abre.

## Links internos

- O menu é igual em todas as páginas e marca a página aberta com `aria-current`.
- As páginas internas têm a trilha "Início > página".
- No início tem a lista das cinco missões e cada uma leva direto para o resumo dela (por exemplo `missoes.html#apollo-11`).
- Na linha do tempo o nome da missão na tabela também leva para o resumo.
- O texto do link diz para onde ele vai, sem "clique aqui".

## Lighthouse antes e depois

Rodei o Lighthouse pelo terminal (`npx lighthouse`) no site publicado no GitHub Pages, antes de subir as mudanças e depois. No celular rodei três vezes cada um e usei a nota do meio, porque a internet muda bastante o desempenho (uma das rodadas do antes deu 49).

Página inicial:

| Categoria | Antes (celular) | Depois (celular) | Antes (computador) | Depois (computador) |
|---|---|---|---|---|
| Desempenho | 96 | 98 | 97 | 100 |
| Acessibilidade | 100 | 100 | 100 | 100 |
| Boas práticas | 96 | 100 | 96 | 100 |
| SEO | 91 | 100 | 91 | 100 |

O SEO subiu porque antes faltava a meta description. Boas práticas subiu por causa do erro do favicon.ico.

A comparação de desempenho não é bem justa, porque antes a página inicial tinha as cinco fotos e agora elas estão na página de missões. Antes a página inicial pesava 1.010 KB. Depois a página inicial pesa 4 KB e a de missões, que tem as fotos, pesa 223 KB. A página de missões no celular ficou com 94 de desempenho, 100 de acessibilidade, 100 de boas práticas e 100 de SEO.

Os relatórios completos estão na pasta [lighthouse](lighthouse/). Dá para abrir eles pelo site também, por exemplo https://soaresm-dev.github.io/missoes-espaciais/lighthouse/depois-celular.html
