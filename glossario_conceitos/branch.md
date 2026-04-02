# Branch

Voltar para o [Glossário](README.md).

**Branches** são **ramificações** do histórico de versionamento do Git. Elas são usadas para trabalhar em uma linha de desenvolvimento separada do histórico principal, é outra forma de deixar a linha do tempo mais organizada e concisa. Uma das funcionalidades que tornam o Git o que ele é hoje, é a facilidade em criar branches diferente e fundi-las. Em um fluxo de desenvolvimento real, vários desenvolvedores trabalham em paralelo em funcionalidades diferentes, com as ramificações, cada um pode criar o seu próprio histórico de commits, sem afetar a ramificação principal (que pode estar sendo usada em produção, ou seja sendo usada por clientes daquele software) ou interferir no fluxo de trabalho de outros desenvolvedores. Por fim, os desenvolvedores podem requisitar que suas ramificações sejam fundidas à principal, em um processo chamado de [_merge_](merge.md).

A branch principal é a ramificação original ou primária do seu projeto, ela é comumente chamada de `master` ou `main`, esse nome pode ser configurado com o comando `git config`.

> **TLDR;** Uma branch é uma ramificação do histórico, com seus próprios commits. Isso permite desenvolver funcionalidades em branches separadas, para então, serem combinadas de volta em uma branch principal.

## Referências

[ Livro Fundamentos do Git. "Cap. 3.1 - Branches em poucas palavras](https://git-scm.com/book/pt-br/v2/Branches-no-Git-Branches-em-poucas-palavras)
