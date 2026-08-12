# Ela Decora — Página de Download

Página pública única com a finalidade de permitir que o visitante baixe o aplicativo oficial da marca **Ela Decora**.

## Tecnologias

- HTML5
- CSS3 puro
- JavaScript puro (sem frameworks, sem dependências)

## Estrutura

```
index.html      Estrutura da página (cabeçalho, card central, rodapé)
styles.css      Estilos visuais (cores, layout, responsividade)
script.js       Lógica do botão de download
images/         Local para a logo (images/logo.png)
netlify.toml    Configuração de publicação estática no Netlify
```

## Configurando o link de download

Abra `script.js` e edite a constante `DOWNLOAD_URL`:

```js
// Arquivo hospedado dentro do próprio projeto:
const DOWNLOAD_URL = "aplicativo.apk";

// Ou um link externo:
const DOWNLOAD_URL = "https://SEU-LINK-AQUI";
```

## Adicionando a logo

Coloque o arquivo `logo.png` dentro da pasta `images/`. A página já referencia `images/logo.png` no cabeçalho. Caso o arquivo não esteja presente, um texto "ELA DECORA" é exibido como alternativa automática.

## Executando localmente

Como é uma página estática, basta abrir `index.html` em um navegador, ou servir a pasta com qualquer servidor HTTP simples:

```bash
npx serve .
```

## Publicação

O projeto está pronto para publicação direta no Netlify como site estático (`publish = "."`, definido em `netlify.toml`).
