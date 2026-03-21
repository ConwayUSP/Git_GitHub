# `git restore`

Voltar ao [Guia de Comandos](README.md)

## O que faz?

O comando `git restore` tem a função de restaurar arquivos no seu working directory ou tirá-los da staging area. Assim como o `switch`, ele foi criado para assumir a parte de "restauração de arquivos" que antes era feita de forma confusa pelo `git checkout` e pelo `git reset`.

## Formas de usar

`git restore <nome-do-arquivo>`: descarta as mudanças não salvas de um arquivo, voltando ele para o estado do último commit;
`git restore --staged <nome-do-arquivo>`: tira o arquivo da staging area (desfaz o git add), mas mantém as suas modificações intactas no código;
`git restore --source=<hash-do-commit> <nome-do-arquivo>`: restaura um arquivo específico para a versão exata que ele tinha em um commit antigo.

## Formas de usar (pelo GitHub Desktop)

Pelo programa, para descartar mudanças (equivalente ao primeiro comando), clique com o botão direito sobre o arquivo modificado no painel esquerdo e escolha Discard changes. Para tirar da staging area, basta desmarcar a caixinha de seleção (o checkbox) ao lado do nome do arquivo.

## Formas de desfazer
Cuidado meu chapa! Se você usar apenas git restore <arquivo> (ou o Discard changes do Desktop), as alterações não salvas serão apagadas permanentemente e não há como desfazer. Se usou o `--staged`, basta dar um `git add` novamente.

## Palavras chaves

- `restaurar`, `descartar`, `limpar`, `unstage`, `reverter arquivo`
