# `git cherry-pick`

Voltar ao [Guia de Comandos](README.md)

## O que faz?

O comando `git cherry-pick` tem a função de "pescar" um commit específico de uma branch qualquer e aplicá-lo na branch em que você está. É ideal quando você precisa de uma correção isolada que está em outra branch, mas não quer fazer o merge dela por inteiro.

## Formas de usar

`git cherry-pick <hash-do-commit>`: aplica a mudança daquele commit específico na sua branch atual.

## Formas de usar (pelo GitHub Desktop)

Pelo programa, a função é extremamente visual. Vá na aba History de uma branch, clique sobre o commit desejado, segure, arraste e solte sobre o nome da branch atual no topo da tela.

## Formas de desfazer

- `git cherry-pick --abort`: cancela a operação caso o commit traga conflitos complexos que você não queira resolver no momento;
- `git reset --hard HEAD~1`: se já aplicou o commit localmente e quer desfazê-lo.

## Palavras chaves

- `pescar`, `extrair`, `correção`, `isolado`
