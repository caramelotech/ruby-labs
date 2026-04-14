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

### Exemplos em `examples/`

- Mantenha os exercicios e projetos atualizados
- Adicione contexto suficiente para uma pessoa iniciante executar
