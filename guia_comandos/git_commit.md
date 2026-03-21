# `git commit`

Voltar ao [Guia de Comandos](README.md)

## O que faz?

O comando `git commit` tem a função de "salvar" as mudanças que estão na staging area (adicionadas pelo git add) para o histórico do repositório local. Cada commit funciona como um "ponto de salvamento" ou uma fotografia do projeto naquele momento, acompanhado de uma mensagem que explica o que foi feito.

## Formas de usar

- `git commit -m "Sua mensagem aqui"`: cria um commit com as mudanças da staging area usando a mensagem especificada;
- `git commit -am "Sua mensagem aqui"`: atalho que adiciona todos os arquivos modificados (já rastreados) à staging area e já faz o commit em um único comando;
- `git commit --amend`: abre o editor para você alterar a mensagem do último commit ou adicionar novas mudanças a ele.

## Formas de usar (pelo GitHub Desktop)
Pelo programa, após selecionar os arquivos na caixa da esquerda, basta preencher os campos "Summary" (obrigatório) e "Description" (opcional) no canto inferior esquerdo e clicar no botão azul Commit to [nome-da-branch].

## Formas de desfazer

- `git reset --soft HEAD~1`: desfaz o último commit, mas mantém as suas modificações na staging area (prontas para um novo commit);
- `git reset --hard HEAD~1`: Cuidado! Desfaz o último commit e apaga todas as modificações feitas nele.

## Palavras chaves

- `salva`, `histórico`, `mensagem`, `checkpoint`, `confirma`
