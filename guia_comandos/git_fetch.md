# `git fetch`

Voltar ao [Guia de Comandos](README.md)

## O que faz?

O comando `git fetch` tem a função de ir até o repositório remoto (como o GitHub) e baixar todas as novidades (commits, branches, arquivos) para a sua máquina, mas sem misturar nada com o seu código atual.

Ele é como se fosse a primeira metade do comando git pull (que faz o fetch e logo em seguida o merge). É a forma mais segura de ver o que a sua equipe andou fazendo antes de decidir aplicar essas atualizações no seu working directory.

## Formas de usar

- `git fetch`: baixa as novidades do repositório remoto padrão (geralmente o origin) para atualizar o seu histórico local;
- `git fetch origin <nome-da-branch>`: baixa as atualizações apenas de uma branch específica do servidor;
- `git fetch --all`: baixa as atualizações de todos os repositórios remotos configurados no seu projeto (muito útil se você estiver trabalhando com forks).

## Formas de usar (pelo GitHub Desktop)

Dá para usar através do botão no menu superior central escrito Fetch origin. Você clica nele para o aplicativo "perguntar" à internet se há atualizações. Se o GitHub Desktop encontrar novidades, o botão mudará de nome para Pull origin e mostrará uma setinha para baixo, avisando que agora há coisas prontas para serem mescladas.

## Formas de desfazer

Não se aplica. O `git fetch` é uma operação 100% segura, pois ele não altera os seus arquivos de trabalho. Ele apenas atualiza as referências do seu banco de dados local do Git. Caso você não goste do que baixou, você pode optar por escolher não fazer o merge.

## Palavras chaves

- `baixar`, `verificar`, `atualizar histórico`
