# `git stash`

Voltar ao [Guia de Comandos](README.md) 

## O que faz?

O comando `git stash` tem a função de "guardar na gaveta" temporariamente as mudanças que você fez no seu working directory mas que ainda não estão prontas para um commit. Útil para quando você precisa mudar de branch rapidamente sem perder o trabalho inacabado.

## Formas de usar

- `git stash`: guarda as modificações atuais e limpa o diretório de trabalho;
- `git stash save "mensagem"`: guarda as modificações dando um nome para facilitar a identificação depois;
- `git stash list`: lista todos os stashes guardados na gaveta;
- `git stash pop`: pega o último trabalho guardado, aplica de volta no seu código e remove da gaveta;
- `git stash apply`: aplica o último trabalho guardado, mas o mantém a cópia salva na gaveta.

## Formas de usar (pelo GitHub Desktop)

Pelo programa, se você tentar mudar de branch com mudanças pendentes, aparecerá um pop-up. Escolha Leave my changes on [nome-da-branch] (isso fará o stash). Para restaurar, clique em View stashed changes na base do painel esquerdo.

## Formas de desfazer

- `git stash drop`: apaga permanentemente o trabalho guardado mais recente na gaveta (sem aplicá-lo);
- `git stash clear`: esvazia completamente a gaveta, deletando todos os stashes armazenados.

## Palavras chaves

- `guardar`, `gaveta`, `temporário`, `esconder`
