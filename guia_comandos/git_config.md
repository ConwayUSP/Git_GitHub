# `git config`

Voltar ao [Guia de Comandos](README.md) 

## O que faz?
O comando `git config` tem a função de definir as configurações e preferências do Git na sua máquina. A principal utilidade é identificar você (cadastrar seu nome e e-mail) para que o Git saiba quem é o autor das modificações registradas nos commits.

## Formas de usar

- `git config --global user.name "Seu Nome"`: define o seu nome para todos os projetos da máquina;
- `git config --global user.email "seu@email.com"`: define o e-mail atrelado aos seus commits;
- `git config --list`: lista todas as configurações ativas no momento.

## Formas de usar (pelo GitHub Desktop)

Pelo programa, os dados de autor são puxados automaticamente quando você faz login na conta. Para mudar manualmente, vá em File > Options... (no Mac: GitHub Desktop > Preferences) e acesse a aba Git para preencher os campos.

## Formas de desfazer

Para corrigir, basta rodar o mesmo comando novamente com os dados corretos que ele irá sobrescrever;

Para remover uma configuração definitivamente, use a tag `--unset (ex: git config --global --unset user.name)`.

## Palavras chaves

- `configurar`, `nome`, `email`, `preferências`, `usuário`
