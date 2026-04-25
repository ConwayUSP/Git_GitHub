# `git reflog`

Voltar ao [Guia de Comandos](README.md) 

## O que faz?

O comando `git reflog` (Reference Logs) é como se fosse um salva-vidas de emergência. Ele tem a função de registrar um diário oculto de absolutamente tudo que altera o ponteiro HEAD do seu repositório local. Mesmo que você faça um `git reset --hard` e apague commits do histórico visível, o reflog lembra onde você estava. Ele é usado para recuperar códigos que pareciam perdidos para sempre.

## Formas de usar

- `git reflog`: exibe a lista de todas as movimentações recentes (commits, resets, merges, checkouts), com um identificador no formato HEAD@{numero};
- `git reset --hard HEAD@{numero}`: depois de olhar a lista do `reflog`, você usa esse comando para "teleportar" o seu repositório de volta para aquele estado exato, recuperando o que foi perdido.

## Formas de usar (pelo GitHub Desktop)

O GitHub Desktop não possui uma interface visual para o `reflog`, pois é uma ferramenta de recuperação avançada. Se você fizer uma grande besteira e precisar dele, terá que ir no menu superior Repository > Open in Command Prompt / Terminal e digitar os comandos manualmente.

## Formas de desfazer

Não se aplica para a visualização. Para sair da tela do `reflog` no terminal, basta pressionar a tecla q.

## Palavras chaves

- `diário`, `emergência`, `recuperar`, `historico oculto`, `head`
