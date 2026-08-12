# AGENTS.md

## Propósito do projeto

Página pública estática de download do aplicativo oficial "Ela Decora". Sem backend, sem banco de dados, sem formulários e sem coleta de dados pessoais — a única ação disponível ao visitante é clicar em um botão para baixar o aplicativo.

## Arquitetura

- Site puramente estático: `index.html` + `styles.css` + `script.js`.
- Sem build step, sem framework, sem bundler.
- Publicado no Netlify como estático via `netlify.toml` (`publish = "."`).

## Arquivos-chave

- `index.html` — cabeçalho com logo, card central com título/subtítulo/botão, rodapé.
- `styles.css` — todas as cores e responsividade. As cores da marca são fixas e não devem ser alteradas sem instrução explícita:
  - Rosa principal: `#DB8393`
  - Rosa hover: `#C97183`
  - Fundo: `#FFF9FA`
  - Texto: `#333333` / Texto secundário: `#777777`
- `script.js` — contém a constante `DOWNLOAD_URL`, único ponto de configuração do link/arquivo de download. Suporta tanto arquivo local hospedado no projeto (ex: `aplicativo.apk` na raiz) quanto link externo (URL completa).
- `images/` — pasta destinada à logo (`images/logo.png`). Se ausente, o cabeçalho usa fallback em texto ("ELA DECORA") via `onerror` no `<img>`.

## Convenções e decisões não óbvias

- Não usar roxo, lilás, violeta, azul ou gradientes — restrição explícita de identidade visual da marca.
- Não adicionar formulários, login, campos de dados pessoais, contadores, pop-ups ou redes sociais — a página deve permanecer limitada estritamente ao fluxo de download.
- A "Central de Atualização" é uma funcionalidade do aplicativo em si e não deve ser replicada nesta página.
- `DOWNLOAD_URL` nunca deve ser preenchido com um link inventado; deve permanecer com o placeholder `"COLE_AQUI_O_LINK_DO_ARQUIVO"` até que o link real seja fornecido.
