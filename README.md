# Código Público Brasil: site da organização

Página inicial do projeto [Código Público Brasil](https://github.com/codigo-publico-brasil), publicada com Cloudflare Pages em https://codigopublicobrasil.com.br.

A página apresenta a missão, o caminho do dado, os projetos (com o repositório e a aplicação de cada um), os princípios, as licenças e como participar.

## Como é feito

Uma página única, em HTML e CSS, sem build, framework ou dependência:

```text
public/                 tudo o que é publicado (o Cloudflare só envia esta pasta)
  index.html            conteúdo e estrutura da home
  404.html              página de erro
  tokens.css            cores e fontes como variáveis (as aplicações importam deste endereço)
  theme.js              botões de tema e de compartilhar (único JavaScript; as aplicações copiam)
  sitemap.xml, robots.txt, llms.txt   endereços padrão de buscadores e agentes de IA
  assets/style.css      visual: tema claro e escuro automático, mobile primeiro
  assets/img/           imagem de compartilhamento (1200 × 630) e ícone do celular
  identidade/           guia de identidade visual: logo, cores, tipografia e regras
  identidade/logos/     símbolos em SVG e PNG (organização e projetos)
wrangler.jsonc          aponta o Cloudflare para public/
README.md, AGENTS.md, CLAUDE.md   documentação do repositório (não publicada)
```

`tokens.css` e `theme.js` ficam na raiz do site, e não em subpasta, de propósito: as aplicações importam ou copiam desses endereços.

As fontes (Fraunces, Inter e JetBrains Mono) vêm do Google Fonts.

## Como ver localmente

Requisito: Python 3. Na pasta `public/`:

```bash
cd public
python -m http.server 4173
```

Abra http://localhost:4173.

## Como publicar

Todo push na branch `main` publica o site sozinho, pelo Cloudflare Pages. Não há etapa de build.

## Conteúdo

Os textos seguem as linhas vermelhas do projeto: sem ranking, sem recomendação de voto, sem adjetivos, e todo dado com fonte oficial. Mudanças de texto, de princípios e de links das aplicações devem manter essas regras. Os links das aplicações que ainda não existem mostram o selo "em breve".

## Pendências

Melhorias e decisões abertas ficam nas [issues deste repositório](https://github.com/codigo-publico-brasil/codigopublicobrasil.com.br/issues).
