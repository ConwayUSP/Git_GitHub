# `git revert`

Voltar ao [Guia de Comandos](README.md) 

## O que faz?

O comando `git revert` tem a função de desfazer as mudanças de um commit anterior de forma segura. Em vez de apagar o commit do histórico, ele cria um novo commit que faz o exato oposto das alterações feitas. É a abordagem correta para corrigir erros em ramificações públicas e compartilhadas.

## Formas de usar

- `git revert <hash-do-commit>`: cria um novo commit que anula as alterações feitas no commit especificado.

## Formas de usar (pelo GitHub Desktop)

Pelo programa, vá na aba History, clique com o botão direito no commit que causou o problema e selecione Revert changes in commit. O Desktop criará o commit de reversão automaticamente.

## Formas de desfazer

Como o `revert` cria um novo commit, para desfazê-lo basta fazer o `revert` do `revert`, ou usar `git reset HEAD~1` caso ainda não tenha feito o push para o servidor.

## Palavras chaves

- `desfazer seguro`, `inversão`, `anula`
