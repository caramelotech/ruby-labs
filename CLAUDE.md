# CLAUDE.md

This file provides guidance to Claude Code (claude.ai/code) when working with code in this repository.

## Overview

Ruby Labs é um repositório educacional voltado para iniciantes em programação que desejam aprender Ruby - tanto a linguagem em si quanto seu uso em automação de testes. O site é gerado com Astro + Starlight e publicado em `https://caramelotech.com.br/ruby-labs/`.

## Commands

```bash
npm install       # instala dependências
npm run dev       # servidor local em http://localhost:4321
npm run build     # build de produção
npm run preview   # visualiza o build localmente
```

## Architecture

- `src/content/docs/` - anotações e estudos publicados no site (Markdown/MDX)
- `examples/` - exemplos de código, exercícios e projetos práticos (não publicados no site)
- `astro.config.mjs` - configuração do Astro e Starlight (sidebar, social links, base path)
- `src/styles/custom.css` - customizações visuais

## Deployment

O deploy é feito automaticamente via GitHub Actions ao fazer push em `main`. O workflow está em `.github/workflows/deploy.yml`. O campo `base: '/ruby-labs'` em `astro.config.mjs` deve ser mantido - todos os links internos precisam incluir esse prefixo.

## Content conventions

- Idioma: português (pt-BR)
- Frontmatter obrigatório:
  ```md
  ---
  title: "Título da nota"
  description: "Resumo curto explicando o foco da página."
  lastUpdated: 2026-01-01
  sidebar:
    order: 1
  tags: ["ruby", "tema", "iniciante"]
  ---
  ```
- Não repita o `title` como `# h1` - o Starlight renderiza automaticamente
- Use `##` e `###` para seções
- Prefira explicações curtas e progressivas

## sidebar.order rule

**`sidebar.order` é sequencial por diretório**, não global. A ordem entre seções é controlada pelo array `sidebar` em `astro.config.mjs`. Dentro de cada pasta, numere os arquivos a partir de 1.

Para adicionar uma nova seção superior (ex: `nova-categoria/`):
1. Crie o diretório em `src/content/docs/nova-categoria/`
2. Adicione um arquivo `index.md` como página de entrada
3. Adicione uma entrada `autogenerate` em `astro.config.mjs`:
   ```javascript
   {
     label: "Título da Seção",
     autogenerate: { directory: "nova-categoria" },
   }
   ```
