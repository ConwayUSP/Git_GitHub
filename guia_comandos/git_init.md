# `git init`

Voltar ao [Guia de Comandos](README.md)

## O que faz?

- O comando git init tem a função de inicializar um novo repositório Git localmente. Ele cria um diretório oculto chamado .git na sua pasta atual, que passa a monitorar e armazenar todo o histórico de controle de versão daquele projeto a partir de então.

## Formas de usar

- `git init`: transforma o diretório atual em um repositório Git;
- `git init <nome-do-projeto>`: cria uma nova pasta com o nome especificado e já inicializa um repositório Git dentro dela.

## Formas de usar (pelo GitHub Desktop)

Pelo programa, acesse o menu superior e vá em File > New repository... (ou pressione Ctrl + N). Preencha o nome, a descrição, escolha o caminho no seu computador e clique no botão "Create repository".

## Formas de desfazer

Para "desfazer" a inicialização, basta apagar a pasta oculta .git que foi criada dentro do diretório do seu projeto (no terminal de comandos: `rm -rf .git`). Isso removerá todo o rastreamento do Git, mas manterá seus arquivos intactos.

## Palavras chaves

- `inicializa`, `cria`, `repositório`, `começar`, `novo projeto`
