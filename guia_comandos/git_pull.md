# `git pull`

Voltar ao [Guia de Comandos](README.md)

## O que faz?
O comando `git pull` tem a função de baixar as mudanças do repositório remoto (do GitHub, por exemplo) e mesclá-las automaticamente com o seu repositório local. Ele une dois processos: baixar os dados (`git fetch`) e mesclar com o seu código (`git merge`).

## Formas de usar

- `git pull`: atualiza a sua branch atual com as novidades da branch remota correspondente;
- `git pull origin <nome-da-branch>`: puxa o código de uma branch específica do repositório remoto.

## Formas de usar (pelo GitHub Desktop)

Pelo programa, se houver atualizações no servidor, o botão superior central mostrará Pull origin acompanhado de uma setinha para baixo e a quantidade de commits pendentes. Basta clicar nele.

## Formas de desfazer
Se o `git pull` trouxer mudanças que geram conflitos e você quiser recuar, use `git merge --abort` para cancelar a junção do código.

## Palavras chaves

- `baixar`, `atualizar`, `trazer`, `sincronizar`, `download`
