# `git rebase`

Voltar ao [Guia de Comandos](README.md) 

## O que faz?
O comando `git rebase` tem uma função similar ao merge (juntar código), mas o faz reescrevendo o histórico. Ele pega os commits da sua branch atual e os aplica no topo de outra branch base. Isso cria um histórico de projeto perfeitamente linear, sem commits de junção adicionais.

## Formas de usar

`git rebase <nome-da-branch>`: move todos os commits da sua branch atual para o topo da branch especificada;
`git rebase -i HEAD~3`: abre o rebase interativo para os últimos 3 commits, permitindo unir (squash), alterar ou deletar commits antes de enviá-los.

## Formas de usar (pelo GitHub Desktop)
Pelo programa, vá ao menu superior Branch > Rebase current branch.... Escolha a branch base. O programa cuidará do processo e pedirá para resolver conflitos passo a passo, caso existam.

## Formas de desfazer
`git rebase --abort`: cancela a operação de rebase em andamento (útil caso empaque na resolução de conflitos) e retorna tudo ao estado original.

## Palavras chaves

- `linear`, `reescrever`, `topo`, `histórico limpo`
