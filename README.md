# Ruby Labs

Repositorio voltado para iniciantes na programacao que desejam aprender Ruby como linguagem de programacao.

## O que voce vai encontrar

- Anotacoes sobre fundamentos de Ruby
- Materiais introdutorios para automacao de testes com Ruby
- Exercicios para fixar conceitos
- Projetos pequenos para praticar

## Estrutura do repositorio

```text
ruby-labs/
├── src/content/docs/   -> Anotacoes e estudos publicados no site
├── examples/           -> Exemplos de codigo, exercicios e projetos praticos
└── .github/            -> Workflows, templates e guias de contribuicao
```

## Como usar

1. Comece pelas notas em `src/content/docs/`
2. Leia [Introducao ao Ruby](src/content/docs/01-introducao-ruby.md)
3. Avance para [Ruby para Automacao de Testes](src/content/docs/02-ruby-para-automacao-de-testes.md)
4. Resolva os desafios em `examples/exercises.md`
5. Experimente o projeto em `examples/projects.md`

## Rodando localmente

```bash
npm install
npm run dev
```

O servidor local fica em `http://localhost:4321`.

Outros comandos uteis:

```bash
npm run build
npm run preview
```

Versao publicada:

`https://caramelotech.github.io/ruby-labs`

## Adicionando notas

Novas anotacoes devem ser criadas em `src/content/docs/`.

Exemplo de frontmatter padrao Starlight:

```md
---
title: "Titulo da nota"
description: "Resumo curto explicando o foco da pagina."
lastUpdated: 2026-01-01
sidebar:
  order: 3
tags: ["ruby", "tema", "iniciante"]
---
```

## Contribuicao

Contribuicoes sao bem-vindas. Veja o [Guia de Contribuicao](.github/CONTRIBUTING.md) para detalhes.

## Licenca

MIT
