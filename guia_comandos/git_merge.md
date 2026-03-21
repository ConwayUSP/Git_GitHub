# `git merge`

Voltar ao [Guia de Comandos](README.md) 

## O que faz?

O comando `git merge` tem a função de juntar o histórico de duas ramificações. Ele pega o trabalho concluído em uma branch (como uma feature) e o funde na sua branch atual (como a main ou develop), combinando as linhas de código.

## Formas de usar

- `git merge <nome-da-branch>`: funde a branch especificada para dentro da branch em que você está no momento.

## Formas de usar (pelo GitHub Desktop)

Pelo programa, vá ao menu superior Branch > Merge into current branch.... Uma janela abrirá pedindo para selecionar qual branch você deseja "puxar" para dentro da atual. Selecione e clique em "Create a merge commit".

## Formas de desfazer

- `git merge --abort`: se ocorrerem conflitos durante o processo e você quiser cancelar antes de finalizar, este comando cancela o merge e volta ao estado anterior;

- `git reset --hard HEAD~1`: se o merge já foi finalizado e commitado localmente, isso apagará o commit de merge.

## Palavras chaves

- `juntar`, `mesclar`, `fundir`, `combinar`, `conflitos`
