# Staging Area

Voltar para o [Glossário](README.md).

**Staging Area** (sem uma boa tradução) é uma zona intermediária, onde você decide quais alterações serão trazidas do [Working Directory](working_directory.md) para o estágio de [Repositório](repositorio.md).

Nessa zona intermediária você adiciona alterações do working directory, através do comando [`git add`](../guia_comandos/git_add.md). Essa zona serve para você organizar de maneira lógica o conteúdo do seu [_commit_](commit.md). Por exemplo, você está num projeto onde você criou duas novas pastas, cada uma com uma funcionalidade ou código diferente, ao invés de salvar o estado do projeto de uma vez só, você decide salvar cada uma individualmente. Desse modo, caso a segunda pasta dê problema (um bug por exemplo) e você precise voltar uma versão, não vai perder os conteúdos da primeira pasta (que está funcionando perfeitamente). Assim, você move apenas a primeira pasta para a staging area, para que ela seja _commitada_, e depois, repete para a segunda pasta.

Em outras palavras a Staging Area permite:

- Organizar de maneira lógica o seu histórico de versões.
- Revisar as alterações antes de fazer um commit, pois você decide o que entra na staging area.
- Adicionar gradualmente as suas alterações através de pequenos commits.

> **TLDR;** Staging Area é uma zona intermediária, para você adicionar manualmente as alterações que você quer salvar em um commit. Utilize `git add` para adicionar alterações e `git status` para ver o que foi alterado.

## Referências

[Santosh Aymar. "Working Directory vs Staging Area vs Repository](https://medium.com/@santoshyerubandi/working-directory-vs-staging-area-vs-repository-0d9e6b7b872c)
