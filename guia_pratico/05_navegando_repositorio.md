# Navegando no Repositório

## HEAD

Para iniciarmos o conceito de navegação, é importante falar sobre o `HEAD`. Esse cara é um ponteiro especial, quase como um adesivo, que aponta para o commit atual, indicando onde você está. Se você navega para uma branch, o `HEAD` se move para apontar para essa branch, que por sua vez aponta para o último commit dela mesma. Quando você faz um *commit* em uma branch, o `HEAD` se move para apontar para esse novo commit.

![repositório mostrando o HEAD apontando para a branch main](./prints/head-normal.png)

Porém, quando você navega para um commit específico, o `HEAD` se torna "detached", ou seja, ele não aponta para nenhuma branch, mas sim diretamente para aquele commit. Isso é útil para inspeção e testes, mas se você quiser fazer alterações, é melhor criar uma nova branch a partir desse ponto para evitar confusões futuras. JAMAIS, em hipótese alguma, faça commits sem estar em uma branch, pois todo seu trabalho pode ser perdido. `Commits` feitos fora de uma branch são chamados de "orphaned commits", e eles serão descartados pel o Git após um período de tempo. Fique tranquilo que mais para frente aprenderemos a recuperar possíves commits que se perderam por engano (mas tente não perdê-los!).

![repositório mostrando o HEAD apontando para um commit específico, sem estar em nenhuma branch](./prints/head-detached.png)

## Iniciando navegação

Vamos de fato começar a aprender a navegar dentro do repositório. Antes de mais nada, vamos simular um fluxo de trabalho real e incrementar a `main` com mais alguns commits. Como já foi abordado antes, é muito comum que as `branchs` cresçam de forma independente, de forma paralela, e por isso é muito importante que você evite ao máximo mexer nos mesmos arquivos em diferentes branchs, pois isso pode gerar conflitos obscuros, que serão tratados mais para frente. No nosso caso, vamos simular isso simplesmente criando mais arquivos `.txt`, por que não? Para isso, vamos nos certificar de que estamos na `main` usando o comando `git checkout main`
Feitos os commits, nosso repositório irá se parecer mais ou menos com isso aqui: uma árvore que possui um galho principal e outro que surge a partir do primeiro nó (commit).

![repositório sendo mostrado como uma arvore, com três commits no galho main e dois no galho teste](./prints/tree.png)

Agora que temos mais alguns commits para brincar, vamos de fato para o que interessa. Um dos comandos para transitar já foi abordado e é o próprio [`git checkout`](../glossario_comandos/git_checkout.md). No entanto, nós só o utilizamos para andar entre `branchs` e ignoramos uma função muito importante dele: a de andar entre commits. Imagine que você está trabalhando numa aplicação e, de repente, percebe que um bug sinistro quebrou tudo. Você, que é um programador muito sapiente, decide voltar alguns commits atrás para descobrir a partir de que ponto o código simplesmente parou de funcionar. Para isso, basta usar o comando `git checkout <hash-do-commit>`. Esse tal de `hash` nada mais é que o CPF do commit, um código de identificação único que o Git gera para cada commit. Para descobrir qual é o hash de um bendito commit, basta usar o comando [`git log --oneline`](../glossario_comandos/git_log.md) e procurar por ele. Com o `--oneline`, o log fica mais compacto e fácil de ler, mostrando apenas um pedacinho do hash (seis caracteres) e a mensagem do commit.

![print do comando git log, mostrando os commits e seus respectivos hashes](./prints/log.png)

Após copiar o hash do commit que você quer visitar, basta usar o `git checkout <hash-copiada>` para ir até ele. E pronto! Você está lá, vendo o estado do repositório exatamente como ele estava naquele momento. Contudo, lembre-se do que já foi dito: o `HEAD` está "detached", ou seja, ele não aponta para nenhuma branch. Se realmente quiser fazer alterações a partir desse ponto, é melhor criar uma branch nova com o comando já ensinado e depois fazer o checkout para essa nova branch, para evitar perder seu trabalho.

Além do `git checkout`, outro comando que cumpre a exata mesma função é o `git switch`. Ele é um comando mais recente e foi introduzido para tornar a navegação entre branches e commits mais intuitiva. Para usá-lo, basta usar o comando `git switch <hash-do-commit>`. Se você se aprofundar, verá que eles possuem algumas diferenças bem sutis, mas para o nosso propósito de navegar entre commits, ambos funcionam da mesma forma. Use o que achar melhor!

Porém, você verá que existem casos que saber o hash do commit não é tão útil assim (ou simplesmente não é prático). Imagine que você quer voltar para o commit anterior, ou seja, para o commit pai do commit atual. Para isso, basta usar o comando `git checkout HEAD^` ou `git switch HEAD^`. O `HEAD^` é uma forma de referenciar o commit pai do `HEAD` de forma prática e rápida, sem precisar copiar hashs. Se quiser voltar dois commits, basta usar `HEAD^^`, e assim por diante. No entanto, se você quiser voltar mais ainda, ficar digitando `^` pode não ser muito legal, então existe uma forma mais prática de fazer isso: `HEAD~n`, onde `n` é o número de commits que você quer voltar. Por exemplo, `HEAD~3` te leva três commits para trás. Essa é uma maneira super eficiente de navegar para trás no histórico do seu repositório, e você verá que pode aplicar esse conceito não só na navegação, mas também em outros comandos que veremos mais para frente. 
