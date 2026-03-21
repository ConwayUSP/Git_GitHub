# `git branch`

Voltar ao [Guia de Comandos](README.md)

## O que faz?

O comando `git branch` tem a função de listar, criar ou excluir ramificações (branches) no seu repositório. Branches são linhas independentes de desenvolvimento que permitem criar novos recursos ou corrigir bugs sem afetar a ramificação principal (main ou master).

## Formas de usar

- `git branch`: lista todas as branches locais e destaca em qual você está no momento;
- `git branch <nome-da-branch>`: cria uma nova branch com o nome especificado, mas não muda para ela;
- `git branch -d <nome-da-branch>`: exclui de forma segura uma branch local (apenas se o merge já tiver sido feito);
- `git branch -D <nome-da-branch>`: força a exclusão de uma branch, mesmo que ela tenha mudanças não mescladas.

## Formas de usar (pelo GitHub Desktop)

Pelo programa, clique no menu superior central (Current Branch) e depois no botão New Branch. Para deletar, certifique-se de estar na branch que quer apagar e vá no menu superior Branch > Delete....

## Formas de desfazer

Se você criou uma branch sem querer, basta deletá-la com `git branch -d <nome-da-branch>`.

## Palavras chaves

- `ramificação`, `listar`, `criar`, `deletar`
