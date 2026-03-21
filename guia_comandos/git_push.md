# `git push`

Voltar ao [Guia de Comandos](README.md) 

## O que faz?

O comando `git push` tem a função de enviar os commits que você fez no seu repositório local (na sua máquina) para o repositório remoto (no GitHub, GitLab, etc.). É o comando que torna o seu trabalho acessível para o resto da equipe.

## Formas de usar

- `git push`: envia as mudanças da branch atual para a correspondente no repositório remoto;
- `git push -u origin <nome-da-branch>`: envia uma branch recém-criada localmente para o remoto pela primeira vez, criando o vínculo (-u de upstream);
- `git push --force (ou -f)`: Cuidado extremo! Força o envio das suas modificações, sobrescrevendo o histórico do servidor remoto. Só use se tiver absoluta certeza do que está fazendo.

## Formas de usar (pelo GitHub Desktop)

Pelo programa, basta clicar no botão azul no menu superior central que diz Push origin (ele indicará com uma setinha para cima quantos commits estão aguardando envio).

## Formas de desfazer

Desfazer um push é complexo porque a alteração já foi para a internet. Geralmente envolve usar git revert localmente e dar um novo git push para corrigir, ou (em casos extremos e isolados) arrumar localmente e usar git push --force.

## Palavras chaves

- `enviar`, `remoto`, `subir`, `upload`, `origin`
