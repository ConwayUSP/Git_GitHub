# `git checkout`

Voltar ao [Guia de Comandos](README.md) 

## O que faz?

O comando `git checkout` tem a função de mudar de uma branch para outra. Ele atualiza os arquivos no seu working directory para refletir a versão exata da branch que você escolheu. (Nota: nas versões mais recentes do Git, vem sendo substituído pelos comandos `git switch` e `git restore`, porém o `git checkout` ainda é muito útil e é extremamente válido utilizá-lo).

## Formas de usar

- `git checkout <nome-da-branch>`: muda para a branch especificada;
- `git checkout -b <nome-da-branch>`: cria uma nova branch e já muda para ela imediatamente (atalho muito utilizado);
- `git checkout -- <nome-do-arquivo>`: descarta as mudanças não "commitadas" de um arquivo, restaurando-o para o último estado salvo.

## Formas de usar (pelo GitHub Desktop)

Pelo programa, basta clicar no menu superior central (Current Branch) e clicar no nome da branch para a qual você deseja mudar. O GitHub Desktop fará a transição automaticamente.

## Formas de desfazer

Para desfazer uma mudança de branch, basta rodar `git checkout <branch-anterior>` para voltar de onde veio.

## Palavras chaves

- `mudar`, `trocar`, `navegar`
