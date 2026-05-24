# HEAD

Voltar para o [Glossário](README.md).

No Git, o `HEAD` é a referência para o estado atual do seu diretório de trabalho, ou seja, onde você está agora. Normalmente, o HEAD aponta para o nome da [branch](branch.md) em que você está trabalhando (como a `main`), e a branch, por sua vez, aponta para o último [commit](commit.md) dela. Se você fizer um novo commit, a branch avança e o HEAD a acompanha. No entanto, se você usar `git checkout` para navegar até um commit antigo, o HEAD se desconecta da branch e passa a apontar diretamente para esse commit, entrando no estado conhecido como `Detached HEAD`.

> Cuidado: qualquer commit feito durante o estado `Detached HEAD` não está salvo na história de nenhuma branch, e portanto será perdido assim que você der `git checkout` para outro commit ou branch.

![Lista ligada de commits, com a HEAD sendo o ponteiro-cabeça](./assets/commit-history.png)

Fonte: GeeksforGeeks.

> **TLDR;** O `HEAD` aponta para o commit ou branch em que o seu diretório de trabalho está neste exato momento.

## Referências

[GeeksforGeeks. "Git - Head"](https://www.geeksforgeeks.org/git/git-head/)
[LearnThatStack - Git Will Finally Make Sense After This](https://www.youtube.com/watch?v=Ala6PHlYjmw)
