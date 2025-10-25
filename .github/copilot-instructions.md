## Instruções rápidas para agentes AI

Este repositório é um site estático (Portfólio) composto por HTML e CSS puro. Use estas instruções para ser produtivo rapidamente ao editar, revisar ou sugerir mudanças.

- Estrutura principal: arquivo de entrada `index.html`. Estilos divididos em `globals.css` (variáveis, tipografia, reset) e `style.css` (componentes/sections).
- Ativos (imagens/ícones) ficam em `assets/` e `assets/icons/` — mantenha referências relativas como `./assets/...` ao editar paths.

Padrões e convenções encontrados

- Componentização por seção: HTML usa seções com id (`#intro`, `#projects`, `#services`, `#contact`) e classes correspondentes (`.intro`, `.projects`, `.services`, `.contact`). Ao adicionar novo conteúdo, siga esse padrão: uma `<section id="nome" class="nome">` com um `header` e containers internos.
- Classes utilitárias de tipografia: use `.title_lg`, `.title_md`, `.title_sm`, `.subtitle`, `.text_md`, `.text_sm` para manter tipografia consistente — definidas em `globals.css`.
- Containers e cards: `.container`, `.projects_container`, `.cards`, `.services_container` já implementam responsividade por flex-wrap; estenda esses blocos ao criar novos componentes.
- Ícones: o projeto usa Phosphor Icons via CDN (link em `index.html`). Use classes `ph ph-nome-do-ícone` para inserir ícones.

Exemplos concretos (copiar/editar quando relevante)

- Adicionar um novo card de projeto: copie um bloco `.cards` dentro de `.projects_container` e atualize `img`, `h3.title_sm`, `p.text_sm` e `a.text_sm`.
- Link externo: todos os links externos usam `target="_blank"`. Preserve isso quando o link for para outro domínio.

Fluxo de desenvolvimento e dicas práticas

- Não há build step; editar arquivos HTML/CSS e abrir `index.html` no navegador é suficiente. Para desenvolver localmente com recarregamento ao salvar, use uma extensão/editor que sirva arquivos estáticos (por exemplo Live Server no VS Code).
- Ao alterar imagens em `assets/`, verifique caminhos relativos e nomes (case-sensitive em ambientes \*nix). No Windows os paths funcionam, mas tenha atenção ao deploy (Vercel/Netlify são case-sensitive).

Contribuições e estilo

- Mantenha a organização visual: use as classes utilitárias de tipografia e cores CSS variables definidas em `:root` (em `globals.css`) — `--red`, `--purple`, `--blue`, etc.
- Evite adicionar frameworks ou pré-processadores sem autorização explícita. Este projeto é propositalmente simples e depende de CSS puro.

Arquivos chave para referência rápida

- `index.html` — estrutura do site e uso de ícones/CDN
- `globals.css` — variáveis, resets e regras tipográficas
- `style.css` — regras por seção e componentes (cards, containers, links)

Seção de verificação rápida antes de abrir PR

1. Verifique se classes utilitárias foram usadas (tipografia e containers).
2. Confirme paths de imagens em `assets/` e `assets/icons/`.
3. Teste o HTML no navegador (abrir `index.html`).

Se algo ficar ambíguo, pergunte ao mantenedor quais convenções seguir (ex.: adicionar novos breakpoints ou alterar tipografia global).

Por favor, diga onde quer que eu foque: corrigir acessibilidade, otimizar imagens, criar componentes reutilizáveis, ou gerar PRs com mudanças propostas.
