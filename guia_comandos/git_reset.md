# `git reset`

Voltar ao [Guia de Comandos](README.md) 

## O que faz?
O comando `git reset` tem a função de "voltar no tempo". Ele desfaz commits movendo o ponteiro da sua branch para um momento anterior no histórico. Ele pode preservar as alterações no seu código para você trabalhar nelas novamente ou descartá-las permanentemente.

## Formas de usar

- `git reset <hash-do-commit> (ou --mixed)`: volta para o commit especificado, desfaz os commits seguintes, mas mantém o código modificado no seu working directory;
- `git reset --soft <hash-do-commit>`: semelhante ao acima, mas coloca as mudanças diretamente na staging area, prontas para um novo commit;
- `git reset --hard <hash-do-commit>`: Cuidado! Volta para o commit especificado e destrói permanentemente qualquer alteração de código feita após ele.

## Formas de usar (pelo GitHub Desktop)
Pelo programa, vá na aba History, clique com o botão direito no commit mais recente e selecione Undo commit para revertê-lo localmente de forma segura.

## Formas de desfazer
Se você fez um `reset --hard` acidentalmente, o comando `git reflog` mantém um diário temporário que pode ajudar a recuperar o código, mas exige conhecimento avançado.

## Palavras chaves

- `voltar`, `desfazer commit`, `ponteiro`
