# `git add`

Voltar ao [Guia de Comandos](README.md) 

## O que faz?

O comando `git add` tem a função de adicionar as mudanças feitas no seu [working directory](../glossario_conceitos/working_directory.md) para a [staging area](../glossario_conceitos/staging_area.md). Ele é o responsável por selecionar quais mudanças você quer enviar para o repositório, ou seja, quais mudanças você quer que façam parte do seu próximo commit.

## Formas de usar

- `git add <nome-do-arquivo>`: adiciona UM arquivo específico;
- `git add <arquivo1> <arquivo2> <arquivo3>`: adiciona VÁRIOS arquivos específicos;
- `git add <caminho-especifico>`: adiciona todos os arquivos modificados dentro de um caminho específico;
- `git add .`: adiciona todos os arquivos modificados;
 
## Formas de usar (pelo GitHub Desktop)

Pelo programa, o processo é bem simples: basta selecionar os arquivos que você quer adicionar para o próximo commit através da caixinha de seleção à esquerda.

## Formas de desfazer

- `git reset <nome-do-arquivo>`: remove um arquivo específico da *staging area*;
- `git restore --staged <nome-do-arquivo>`: também remove um arquivo específico da *staging area*;

## Palavras chaves

`adiciona`, `staging area`, `seleciona`, `mudança`
