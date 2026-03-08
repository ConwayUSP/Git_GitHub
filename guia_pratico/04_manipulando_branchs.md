# Manipulando Branchs

## Fazendo manualmente

Agora que temos um repositório com um belo [commit](../glossario_conceitos//commit.md), podemos criar uma [branch](../glossario_conceitos/branch.md). Para entendermos melhor o que é uma *branch*, vamos imaginar que o repositório é como um a ávore, e a cada commit essa árvore cresce em tamanho. Criar uma *branch* significa acrescentar um galho nessa árvore, de forma que tanto o galho principal quanto esse novo possam crescer paralelamente, sem um interferir no outro. Durante o desenvolvimento de projetos, é comum que features diferentes sejam feitas em branchs diferentes, por equipes diferentes. Pensando num website, por exemplo, podemos criar uma branch somente para trabalhar na página principal, outra para trabalhar na página "sobre" e outra para a página de contato. Sua utilidade é justamente poder separar melhor o trabalho e gerar menos conflitos durante o desenvolvimento. Outra coisa muito legal das branchs é que podemos transitar entre elas (literalmente pular de galho em galho). Assim, podemos ver o mesmo projeto em diferentes estados, com diferentes coisas sendo implementadas ao mesmo tempo. Mais para frente, veremos boas práticas para se criar branchs, mas por enquanto isso é o bastante

Dessa forma, criar uma branch é extremamente simples: basta digitarmos [`git branch <nome-da-branch>`](../guia_comandos/git_branch.md) e pronto, ela foi criada! Caso tenha dúvida se o comando deu certo, basta usar o comando [`git branch`](../guia_comandos/git_branch.md) novamente, mas sem o nome da branch, que ele irá listar as branchs existentes. O asterisco indica qual é a branch atual, ou seja, em qual branch estamos trabalhando.

![terminal listando branchs e indicando a branch atual](./prints/branch_list.png)

Contudo, não é porque a branch foi criada que ela será automaticamente utilizada. Para fazer isso, precisamos "transitar" para ela usando o [`git checkout <nome-da-branch>`](../guia_comandos/git_checkout.md). Ao usar `git branch` novamente, podemos ver que o asterisco mudou de lugar, indicando que agora estamos trabalhando na nova branch. A partir de agora, todos os commits que fizermos estarão **exclusivamente** nessa branch, ou seja, não afetarão a branch principal. Para testar isso, vamos criar alguns novos arquivos, modificá-los e fazer alguns *commits* (lembre-se que aqui não estamos nos preocupando com títulos adequados, mas no dia a dia é importante se atentar nisso). Depois disso, vamos usar um novo comando: [`git log --oneline`](../guia_comandos/git_log.md). A partir dele, podemos ver um histórico de commits de forma bem resumida.

![terminal mostrando histórico de commits resumido](./prints/branch_log.png)

Agora, vamos voltar para a branch principal usando o `git checkout main` e usar o `git log --oneline` novamente. Talvez você se assuste e se indague: "Meu Deus! Onde estão todos os meus commits?!". Mas calma, eles não sumiram de fato. É justamente esse o poder das branchs: todas nossas mudanças ficaram na outra branch, enquanto essa aqui, a principal, permaneceu intacta. Cada branch irá possuir o seu próprio histórico de commits, e o `git log` irá mostrar apenas os seus respectivos commits.

![terminal mostrando histórico de commits resumido da branch principal](./prints/branch_log_main.png)

## Pelo GitHub Desktop

Pelo programa, o processo é bem simplificado também: na aba superior, haverá um *Current branch* (branch atual). Clicando nesse botão, haverá a listagem de todas as branchs existentes. No nosso caso, haverá apenas a branch principal - a *main*. Para criar uma, basta clicarmos em *New branch* (nova branch).

![interface listando branchs e com botão de criar nova](./prints/branch_create.png)

Depois disso, uma outra tela muito simples abrirá apenas para indicar qual o nome da branch - só isso!

![interface com nome da branch a ser criada](./prints/branch_name.png)

Por último, para simularmos o `git checkout` e trocarmos de branch, basta clicarmos novamente no botão que lista todas as `branchs` e clicar naquela para a qual queremos transitar. E pronto, mudamos de branch!

![interface listando branchs](./prints/branch_list_gd.png)
