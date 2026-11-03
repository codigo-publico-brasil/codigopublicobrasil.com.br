# Código Público Brasil: site da organização

Página inicial do projeto [Código Público Brasil](https://github.com/codigo-publico-brasil), publicada com Cloudflare Pages em https://codigopublicobrasil.com.br.

A página apresenta a missão, o caminho do dado, os projetos (com o repositório e a aplicação de cada um), os princípios, as licenças e como participar.

## Como é feito

Uma página única, em HTML e CSS, sem build, framework ou dependência:

```text
Página
  index.html            conteúdo e estrutura da home
  404.html              página de erro
  assets/style.css      visual: tema claro e escuro automático, mobile primeiro
  tokens.css            cores e fontes como variáveis (as aplicações importam deste endereço)
  theme.js              botões de tema e de compartilhar (único JavaScript; as aplicações copiam)

Identidade
  identidade/           guia de identidade visual: logo, cores, tipografia e regras
  identidade/logos/     símbolos em SVG (organização e projetos)

Busca, redes sociais e agentes de IA
  og.png                imagem de compartilhamento (1200 × 630)
  apple-touch-icon.png  ícone para a tela inicial do celular
  sitemap.xml, robots.txt, llms.txt
```

`tokens.css`, `theme.js`, `og.png` e `apple-touch-icon.png` ficam na raiz de propósito: as aplicações e as redes sociais usam esses endereços.

As fontes (Fraunces, Inter e JetBrains Mono) vêm do Google Fonts.

## Como ver localmente

Requisito: Python 3. Na raiz do repositório:

```bash
python -m http.server 4173
```

Abra http://localhost:4173.

## Como publicar

Todo push na branch `main` publica o site sozinho, pelo Cloudflare Pages. Não há etapa de build.

## Conteúdo

Os textos seguem as linhas vermelhas do projeto: sem ranking, sem recomendação de voto, sem adjetivos, e todo dado com fonte oficial. Mudanças de texto, de princípios e de links das aplicações devem manter essas regras. Os links das aplicações que ainda não existem mostram o selo "em breve".

## Pendências

Melhorias e decisões abertas ficam nas [issues deste repositório](https://github.com/codigo-publico-brasil/codigopublicobrasil.com.br/issues).
