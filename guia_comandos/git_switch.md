# `git switch`

Voltar ao [Guia de Comandos](README.md)

O que faz?
O comando `git switch` tem a função exclusiva de mudar de uma ramificação (branch) para outra. Ele foi introduzido nas versões mais recentes do Git* para separar essa tarefa do comando `git checkout` (que fazia muitas coisas diferentes ao mesmo tempo, como trocar de branch e restaurar arquivos, embora como eu mencionei na seção do `git checkout`, não é errado utilizá-lo, o uso dele ainda é válido).

* Para se ter uma ideia, o git checkout existe desde por volta de 2005 nas primeiras versões do git, quando foi criado pelo Linus Torvald, que também o criador do Linux (se você ainda não conhece essa lenda da computação, por favor conheça! https://pt.wikipedia.org/wiki/Linus_Torvalds).
* Já o `git switch` surgiu bem depois, em 2019, na versão Git 2.23.

Formas de usar

- `git switch <nome-da-branch>`: muda para a branch especificada;
- `git switch -c <nome-da-branch>`: cria uma nova branch e já muda para ela imediatamente (o -c significa create);
- `git switch -`: um atalho super útil que faz você voltar para a última branch em que estava (como o botão "voltar" da TV).

## Formas de usar (pelo GitHub Desktop)

Pelo programa, o processo é o mesmo do checkout. Basta clicar no menu superior central (Current Branch) e selecionar o nome da branch para a qual você deseja mudar. O GitHub Desktop faz a transição por baixo dos panos.

## Formas de desfazer

Para desfazer uma mudança de branch, basta usar o atalho `git switc`h - para retornar de onde você acabou de sair.

## Palavras chaves

- `trocar`, `mudar`, `branch`, `navegar`
