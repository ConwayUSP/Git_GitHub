# Working Directory

Voltar para o [Glossário](README.md).

O _Working Directory_ ou _Diretório de Trabalho_ é o seu espaço atual no seu projeto, são os arquivos e pastas que você está editando, excluíndo ou criando, se o [Repositório](repositorio.md) é a sua bancada de trabalho, o _working directory_ é como seus papéis, ferramentas e objetos está distribuídos na mesa.

Ele é a primeira etapa do versionamento do git, onde as alterações feitas ainda não foram salvadas, mas estão refletidas diretamente para você ver. Portanto, você pode fazer criar, deletar e salvar arquivos e pastas, antes de salvá-las no histórico, o que permite experimentar ou testar diversas abordagens sem encher o histórico com versões quebradas, erradas ou que só não façam sentindo.

## Estados no Working Directory

Arquivos podem ter dois estados dentro desse estágio:

1. **Tracked** (reastreado), o Git sabe da existência desses arquivos e está de olho em modificações;
2. **Untracked** (não-rastreado), o Git não sabe (ainda) sobre esses arquivos, geralmente porque você acabou de criá-los e ainda não os commitou.

## Ignorando arquivos

Nem sempre queremos que o Git rastreie todos os arquivos do nosso projeto. Por exemplo, é comum guardar chaves de segurança e informações sigilosas em um arquivo `.env` e você **não** quer que esse arquivo seja exposto de jeito nenhum! Outro exemplo é a pasta `node_modules`, em projetos javascript, essa pasta guarda todas as dependências do seu projeto, portanto, essa pasta pode chegar até _gigas_ de tamanho, e enviar esse tanto de dados pela rede pode demorar muito tempo, dada uma conexão lenta. E como essas dependências podem ser baixadas pela internet separadamente, é muito melhor descartar essa pasta do respositório.

Dito isso, o Git usa um arquivo especial, chamado de `.gitignore` para você descrever que arquivos o Git deve _ignorar_ na hora de rastrear o _working directory_, ao adicionar esse arquivo na raiz do seu projeto, em cada linha você pode colocar o item a ser ignorado, veja o exemplo abaixo.

```sh
# isso é um comentário
.env

# ignora a pasta node_modules
node_modules/

# usamos um * para dizer: ignore todos os arquivos que terminam com .sqlite3
*.sqlite3 # ignora arquivos do banco de dados sqlite

```

> **TLDR;** o Working Directory é o estado atual do seu projeto, onde você faz todas as edições e cria novos arquivos.

## Referências

[Git Scripts. "Git Working Directory"](https://gitscripts.com/git-working-directory)
