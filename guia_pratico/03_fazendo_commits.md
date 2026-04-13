# Fazendo Commits

## Fazendo manualmente

Com o [repositório](../glossario_conceitos/repositório.md) criado, podemos começar a fazer [commits](../glossario_conceitos/commit.md). Tecnicamente, um commit é um nó que aponta para o commit pai (o anterior) e guarda um *snapshot* — uma "print" do estado atual do projeto naquele momento, com todos os arquivos e linhas de código. Ou seja, podemos observar um repositório como sendo basicamente um "grafo" direcionado, sempre apontando pra trás.

Como não iremos trabalhar com nenhuma linguagem específica, o tipo de arquivo que usaremos aqui para fins didáticos será o `.txt`, mas é óbvio que no seu dia dia você terá contato com ínumeras extensões de arquivos. Portanto, crie um no seu repositório e escreva qualquer baboseira dentro. Pelo VSCode, observe que o nome do arquivo ficará em verde na aba lateral, junto a uma letra "U", que significa *Untracked*. Isso quer dizer que o Git detectou que um arquivo surgiu/foi modificado.

![mostrando a aba de arquivos não rastreados](./assets/untracked.png)

Isso pode ser visto melhor através do comando [`git status`](../guia_comandos/git_status.md), o qual te fornece algumas informações valiosas.

![mostrando o status do repositório](./assets/status-01.png)

Portanto, para que nossas incríveis mudanças possam valer de algo, precisamos usar o comando [`git add .`](../guia_comandos/git_add.md) (o ponto "." aqui serve para indicar que queremos adicionar **TODOS** os arquivos da pasta atual (que nesse caso é só o .txt)). Agora, na lateral esquerda, é possível ver que o "U" foi trocado por um "A", que significa *Added*. Antes, as mudanças estavam somente no seu [working directory](../glossario_conceitos/working_directory.md), mas agora elas passaram para a [staging area](../glossario_conceitos/staging_area.md). Talvez você se pergunte qual a utilidade do comando de *adicionar*: não poderíamos simplesmente *commitar* direto? E a resposta é NÃO! A ideia aqui é que você pode e DEVE separar "pedaços" de trabalho (uma mudança num estilo específico, a resolução de um bug, a adição de uma feature, etc.). Manter separado em *commits* diferentes te ajuda a organizar melhor o histórico do seu projeto, facilita a identificação de mudanças específicas e qual desenvolvedor a fez. E como você faz essa separação? Fazendo o `git add` somente dos arquivos que você quer enviar naquele momento! Legal, não?

Novamente, o comando `git status` pode mostrar um pouco mais do que foi feito após o comando.

![mostrando o status do repositório](./assets/status-02.png)

Com a mudança adicionada, podemos *commitá-la* (se acostume com essa junção de português e inglês haha) - o que significa que as mudanças selecionadas a dedo serão finalmente enviadas para o [repositório](../glossario_conceitos/repositório.md). Para tal, usaremos o comando [`git commit -m <mensagem-do-commit>`](../guia_comandos/git_commit.md) (o `-m` aqui é de "mensagem"). A mensagem do commit costuma e deve ser sucinta, descrevendo somente o necessário. Enviado o comando, seu primeiro commit foi feito!

![alt text](./assets/commit-criado.png)

## Pelo GitHub Desktop

Pelo programa, todo esse processo manual fica muito mais simples (mas também muito mais sem graça haha). No dia a dia, é o mais provável que você use, tanto pela facilidade tanto quanto pela praticidade.

Com o programa aberto já no repositório que estamos trabalhando, será possível observar uma aba lateral onde todos os arquivos que foram modificados estarão listados. Para fins didáticos, criei mais um arquivo .txt para incrementar a lista. O equivalente ao `git add` seria selecionar ou não arquivos dessa lista, através da caixinha de seleção à esquerda. Após selecionar somente os arquivos que queremos *commitar*, podemos adicionar um título para o commit, juntamente com sua descrição. E voilà, o `git commit` também foi feito!

![mostrando como fazer o git add e o git commit pelo github desktop](./assets/vs-commit.png)
