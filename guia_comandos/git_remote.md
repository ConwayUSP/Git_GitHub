# `git remote`

Voltar ao [Guia de Comandos](README.md)

## O que faz?

O comando `git remote` tem a função de gerenciar as conexões entre o seu repositório local (na sua máquina) e os repositórios remotos (hospedados em servidores como o GitHub). Pense nele como uma espécie de "agenda de contatos" do seu projeto: ele salva os apelidos (como o famoso origin) e as URLs de onde o seu código deve ser baixado ou enviado.

## Formas de usar

- `git remote -v`: lista todas as conexões remotas configuradas no momento, mostrando os apelidos e as URLs (o -v significa verbose, ou seja, detalhado);
- `git remote add <apelido> <url>`: cria uma nova conexão. O padrão da comunidade é usar o apelido origin para o servidor principal (ex: `git remote add origin https://github.com/usuario/projeto.git`);
- `git remote remove <apelido>`: apaga uma conexão remota do seu repositório local;
- `git remote set-url <apelido> <nova-url>`: altera o endereço (URL) de uma conexão que já existe (muito útil se o repositório mudou de dono ou de link no GitHub).

## Formas de usar (pelo GitHub Desktop)

Pelo programa, o gerenciamento do remoto é bem simplificado. Vá no menu superior Repository > Repository settings... e acesse a aba Remote. Lá você pode visualizar e alterar a URL do seu repositório remoto principal (origin).

## Formas de desfazer

Se você adicionou um remoto com o nome ou a URL errada, não se preocupe. Basta usar o comando `git remote remove <apelido>` para apagar a conexão e começar de novo, ou usar o `git remote set-url <apelido> <url-correta>` para consertar o endereço.

## Palavras chaves

- `conexão`, `servidor`, `origin`, `url`
