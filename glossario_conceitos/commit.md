# Commit

Voltar para o [Glossário](README.md).

Um **Commit** do Git é como uma "foto" de um momento no tempo do seu projeto. O histórico do git é composto de commits que contam a evolução daquele repositório, onde um antecede o outro até chegar no commit mais atual ([HEAD](head.md)) ou no commit original. Cada commit possui uma _string_ _hash_ associada a ele, ex.: `123abc` bem como uma mensagem ou marcador que você, desenvolvedor, pode atribuir, por exemplo: `"adiciona arquivo main.py"`. Com os comandos [`git commit`](../guia_comandos/git_commit.md) e [`git log`](../guia_comandos/git_log.md), você pode criar novos commits e ver o histórico dos mesmos. Além disso, é possível voltar a um commit específico usando o comando [`git checkout`](../guia_comandos/git_checkout.md).

## Mensagens de Commit

Não existe um padrão definido de como você deve escrever as mensagens de um commit. Geralmente elas devem ser curtas e resumir as alterações feitas, para que você e seus colegas possam saber o que é aquela versão ao ler a mensagem. Existe a especificação [Conventional Commits](https://www.conventionalcommits.org/pt-br/v1.0.0/) que busca padronizar o formato de mensagem em projetos, caso ache interessante e útil dê uma olhada.

> **TLDR;** um commit é um retrato de um momento do seu projeto, geralmente com uma mensagem associada. Muitos deles, juntos formam um histórico navegável e permite trazer o estado atual do projeto para versões anteriores.

## Referências

[W3Schools. "Git Commit"](https://www.w3schools.com/git/git_commit.asp)
