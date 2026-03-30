# Merge

Voltar para o [Glossário](README.md).

**Merge** é a operação de combinar duas [branches](branch.md) no Git para combinar uma branch em outra, geralmente a branch principal. O comando que permite fazer essa operação é o [git merge](../guia_comandos/git_merge.md).

Por padrão, quando um merge ocorre um novo commit é incluído na branch principal, com todas as alterações feitas na branch sendo combinada.

## Rebase

**Rebase** é uma operação similar ao merge, contudo ele altera o histórico de commits da branch principal para incluir o histórico da outra branch. Ele é usado quando se quer um histórico linear e simples do projeto. Mas pode ser que ele traga conflitos se muitas branches estão sendo desenvolvidas em paralelo.

## Conflitos

Acontece que combinar duas branches nem sempre é uma operação tão fácil. Pense nisso, o que acontece se duas pessoas alterarem o mesmo local de código em branches diferentes e depois tentarem combiná-las? A resposta para isso é um **Merge Conflict** ou apenas **conflito**, que precisa ser resolvido manualmente por você, o Git ou o Github irão abrir uma interface onde você pode escolher entre uma das duas versões do código ou escrever sua própria versão. Quando todos os conflitos estiverem resolvidos, o merge ocorre normalmente.

> **TLDR;** Merge é a operação de combinar uma branch em outra.

## Referências

[GeeksforGeeks. "Git Merge"](https://www.geeksforgeeks.org/git/git-merge/)
