# Desfazendo Caquinhas

Lá estava você codando furiosamente, criando e se movendo pelas branches como se fosse o Tony Hawk em uma pista de skate até que... BANG!!! ERROS BIZONHOS DO GIT ATINGEM SUA CABEÇA.

Mantenha a calma, geralmente é possível voltar atrás e resolver qualquer caquinha.

Veremos aqui alguns dos problemas mais recorrentes e como corrigi-los.

> Este capítulo é uma adaptação do famoso [Oh Shit, Git!?!](https://ohshitgit.com/)

## MERDA! Quero voltar no tempo!!!

Para isso, você pode usar o `git reflog` em conjunto com o `git reset`. Este combo te possibilita voltar seu repositório local no tempo para um instante no qual algo de muito ruim ainda não tinha acontecido (como um merge mal feito ou a adição de um bug grotesco).

``` sh
# te mostrará uma lista das ações recentes
# feitas em todos os branches. Cada ação terá
# um HEAD@{index} do lado, ache o que vem antes
# da ação catastrófica
git reflog
# agora é só mover o HEAD para aquele momento
git reset HEAD@{index}
```

## MERDA! Esqueci de adicionar essas modificações no meu último commit!!!

Pode ficar tranquilo, desde que você não tenha dado `push` para o repositório remoto ainda, basta você criar um novo `commit` com as flags `--amend --no-edit`. Assim, todas as alterações do novo commit entrarão para o commit anterior, e a mensagem do commit ficará intacta. Contudo, é realmente importante que você ainda não tenha dado `push`, caso contrário esse método não funcionará.

``` sh
# adicione as modificações à área de staging
git add file1.md
# dê o commit!
git commit --amend --no-edit
```

## MERDA! Escrevi caquinha na mensagem do meu último commit!!!

De boa na lagoa, é só usar o `git commit --amend` de novo, dessa vez sem `--no-edit`, e uma aba se abrirá para você editar a mensagem do último `commit`.

``` sh
git commit --amend
```

## MERDA! Esqueci de criar uma nova branch para esse commit, agora ele está na branch errada!!!

Tranquilo como esquilo (desde que você não tenha dado `push`), aqui a gente aplica outro combo insano. Primeiro você vai criar a nova branch com o `git branch`. Depois, é só usar o `git reset` e partir para o abraço.

``` sh
# criando uma nova branch para abrigar seu último commit
git branch nova-branch
# voltando a HEAD 1 commit para trás (o ~ é importante)
git reset HEAD~ --hard
# indo para a branch recém criada, onde seu commit te aguarda
git checkout nova-branch
```

## MERDA! Fiz um commit para a branch errada!!!

Aqui o problema pode até ser um pouco mais sério, mas sempre há salvação. Nós iremos voltar a `HEAD` um pouco, mas com a flag `--soft` para não perder as mudanças que estavam no último commit. Depois, iremos colocar essas mudanças no `stash`, mudar de branch, aplicar de novo as mudanças e por fim refazer o `commit`.

``` sh
# desfazendo um commit mas mantendo as mudanças nos arquivos
git reset HEAD~ --soft
# salvando as mudanças em um potinho
git stash
# indo para a branch certa
git checkout branch-certa
# tirando as mudanças do potinho
git stash pop
# refazendo o commit
git add .
git commit -m "mensagem frenética de commit";
```

## MERDA! Minhas diffs não estão aparecendo!!!

Se você rodou `git diff` para ver suas mudanças desde o último `commit` e nada está sendo exibido, provavelmente é porque você já colocou os arquivos na área de staging com o `git add`. Para ainda assim ver a `diff` sem ter que tirar nada da área de staging, é só rodar o seguinte comando:

``` sh
git diff --staged
```

## MERDA! Preciso desfazer um commit aleatório da minha história!!!

Se você fez uns 30 `commits` em sequência e agora quer desfazer o 18° porque ele introduziu um bug, é só usar o famoso `git revert`.

``` sh
# veja o histórico de commit para encontrar
# o hash do commit feio
git log
# com o revert o git irá criar um novo
# commit que desfaz um commit anterior
git revert [hash]
```

## MERDA! Quero desfazer minhas mudanças num único arquivo!!!

Por algum c*r@lh0 de motivo o `git checkout` te ajuda com isso. Basta fazer o seguinte:

``` sh
# veja o histórico de commit para encontrar
# o hash de um commit com o arquivo intacto
git log
# use o checkout naquele arquivo em específico
git checkout [hash] -- caminho/pro/arquivo
# crie um novo commit
git commit -m "catapimbas"
```

## Foda-se, eu desisto!

Para aqueles que já destroçaram tanto a branch na qual estão trabalhando que já perderam as esperanças, só resta uma opção: recomeçar.

``` sh
git fetch origin
git checkout main
git reset --hard origin/main
git clean -d --force
```


