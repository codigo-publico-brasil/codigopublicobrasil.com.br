**Quanto menos código e menos estrutura, melhor; seja sucinto, mas resolva o problema da melhor forma. Proponha antes de executar.**

Este repositório é o site da organização Código Público Brasil: uma página única em HTML e CSS, publicada pelo Cloudflare Pages. As aplicações (`nocargo`, `quem-decidiu`) e a plataforma de dados (`dado-publico-brasil`) vivem em outros repositórios e em outros servidores; aqui só há a home.

## Regras

- **Sem build, framework ou dependência.** Só HTML e CSS, mais o `theme.js` dos botões de tema e de compartilhar. Não adicione outro JavaScript, gerador de site ou bibliotecas sem proposta aprovada.
- **Idioma:** português do Brasil, em todo texto e comentário.
- **Texto da página:** claro para o público geral e profissional. Sem adjetivos, sem recomendação de voto, sem ranking, sem prometer o que ainda não existe (por exemplo, "todos os dados em um só lugar"). Não altere o texto do topo, os princípios nem a frase "Transparência não é favor, é um direito." sem pedido do usuário.
- **Aplicações que ainda não existem** mostram o selo "em breve" (`<span class="soon">`), não um link. Só troque pelo link quando o usuário informar o endereço.
- **Design:** cores e fontes ficam nas variáveis do `:root` em `tokens.css`. Siga o tema claro e escuro e o layout mobile primeiro; confira nos dois temas e em 375 px de largura.
- **Fontes externas:** hoje vêm do Google Fonts. Não adicione outros serviços de terceiros.

## Publicar

Só publique (push, criar ou alterar repositório, mexer no Cloudflare Pages ou no domínio) quando o usuário pedir. O site é público e um push na `main` o atualiza.

O domínio `codigopublicobrasil.com.br` está ativo no Cloudflare Pages (DNS na Cloudflare, domínio registrado no Registro.br, HTTPS obrigatório).

Pendências e decisões abertas são **issues deste repositório**, não arquivos `.md`.

## SEO e leitura por agentes de IA

- Toda página nova tem `<title>` e `description` próprios, `canonical`, Open Graph, Twitter Card e dados estruturados (JSON-LD), como `index.html`. Entra também no `sitemap.xml` (com `lastmod`) e no `llms.txt`.
- Um único `<h1>` por página, títulos em ordem (h1, h2, h3) e todo conteúdo em HTML puro: o texto não pode depender de JavaScript para existir.
- Ao mudar missão, princípios ou projetos, atualize também o `llms.txt` e o JSON-LD da home, para o resumo não divergir do site.
- `robots.txt` permite tudo, de propósito, inclusive agentes de IA. Não bloqueie rastreadores sem pedido do usuário.
- `assets/img/compartilhamento-1200x630.png` e `assets/img/icone-celular.png` são imagens geradas: refaça se o logo ou o lema mudarem.
- Tudo o que é publicado fica em `public/` (é a única pasta que o Cloudflare envia; documentação e `wrangler.jsonc` ficam fora). Dentro dela, `tokens.css` e `theme.js` ficam na raiz do site, porque os apps dependem desses endereços. Imagens ficam em `assets/img/`.
- Contato institucional: codigopublicobrasil@gmail.com (home, rodapés, JSON-LD e `llms.txt`).
