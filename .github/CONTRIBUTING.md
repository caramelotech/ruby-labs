# Guia de Contribuicao

Obrigado por querer contribuir com o Ruby Labs.

## O que pode ser contribuido

- Melhorias e correcoes nas anotacoes em `src/content/docs/`
- Novos exemplos praticos em `examples/`
- Exercicios adicionais em `examples/exercises.md`
- Projetos praticos em `examples/projects.md`
- Melhorias no site Astro + Starlight

## Processo

1. Crie uma branch a partir de `main` seguindo o padrao:

   ```text
   feature/descricao-curta
   fix/descricao-curta
   docs/descricao-curta
   ```

2. Faca commits atomicos com mensagens no padrao de Conventional Commits.

3. Abra um Pull Request usando o template do repositorio.

## Rodando o site localmente

```bash
npm install
npm run dev
```

O site fica disponivel em `http://localhost:4321`.

## Padroes de conteudo

### Anotacoes em `src/content/docs/`

- Escreva em portugues
- Use frontmatter Starlight completo
- Prefira explicacoes curtas e progressivas

**`sidebar.order` e sequencial por diretorio**, nao global. A ordem entre secoes e controlada pelo array `sidebar` em `astro.config.mjs`. Dentro de cada pasta, numere os arquivos a partir de 1.

Para adicionar uma nova secao superior (ex: `nova-categoria/`):
1. Crie o diretorio em `src/content/docs/nova-categoria/`
2. Adicione um arquivo `index.md` como pagina de entrada
3. Adicione uma entrada `autogenerate` em `astro.config.mjs`:
   ```javascript
   {
     label: "Titulo da Secao",
     autogenerate: { directory: "nova-categoria" },
   }
   ```

### Exemplos em `examples/`

- Mantenha os exercicios e projetos atualizados
- Adicione contexto suficiente para uma pessoa iniciante executar
