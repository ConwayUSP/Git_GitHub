# Configuração Inicial

Essa parte do guia é exclusiva para te ajudar a configurar o Git e o GitHub pela primeira vez. Aqui, você aprenderá como instalar o Git, configurar suas credenciais e conectar seu repositório local ao GitHub. Além das ferramentas principais, você também aprenderá a baixar a instalar o Visual Studio Code, um editor de código leve e poderoso, que possui uma integração incrível com o Git e o GitHub, facilitando muito a sua vida como desenvolvedor; e também o GitHub Desktop, uma interface gráfica para o Git, que torna o processo de gerenciamento de repositórios e colaboração ainda mais simples e intuitivo.

Se você já tem esses softwares instalados e configurados, pode pular para o próximo capítulo sobre [Por Trás dos Panos](./01_por_tras_dos_panos.md).

## Instalação do Visual Studio Code

### Windows

1. Acesse o site a seguir e baixe a versão para Windows: [https://code.visualstudio.com/download](https://code.visualstudio.com/download).
2. Durante a instalação, é recomendável selecionar as seguintes opções:
   1. **Adicionar ao PATH**: marque a opção **Add to PATH** para que o VSCode possa ser acessado diretamente pelo terminal.
   2. **Abrir com Code**: marque a opção **Open with Code** para que você possa abrir pastas e arquivos diretamente no VSCode clicando com o botão direito em qualquer pasta ou arquivo.
3. Após seguir as etapas de instalação, clique em **Install** e aguarde a instalação ser concluída.
4. Se tudo deu certo, o Visual Studio Code já deve estar instalado no seu computador!

### Linux

1. Acesso o site a seguir e escolha a versão .deb ou .rpm, dependendo da sua distribuição: [https://code.visualstudio.com/download](https://code.visualstudio.com/download).
2. Depois de baixar o arquivo, basta clicar duas vezes nele para iniciar a instalação, ou usar o terminal para instalar o pacote, dependendo da sua distribuição.
3. Se tudo deu certo, o Visual Studio Code já deve estar instalado no seu computador!

### Extensões recomendadas

No VSCode, existem inúmeras extensões que podem ajudar a melhorar sua experiência de desenvolvimento. Para acessá-las, clique no ícone de extensões na barra lateral esquerda (ou use o atalho `Ctrl + Shift + X`). Aqui nesse guia, recomendamos as seguintes extensões:

1. **GitLens**: com essa extensão, é possível visualizar o histórico de commits de maneira visual e intuitva, podendo observar quem realizou cada alteração, quando e o que foi alterado. Também é possível fazer push e feth diretamente pelo editor, visualizar branchs, o que está em stash, etc. Enfim, é uma extensão incrível para quem quer ter uma visão mais clara do que está acontecendo no repositório.
2. **GitHub Pull Requests**: através dela, é possível fazer [pull requests](../glossario_conceitos/pull_request.md) diretamente pelo VSCode, sem precisar acessar o site do GitHub. Além disso, é possível revisar pull requests, fazer comentários e aprovar ou solicitar mudanças, tudo isso sem sair do editor!
3. **gitignore**: essa extensão ajuda a criar arquivos .gitignore de forma rápida e fácil, permitindo ignorar arquivos e pastas que não devem ser versionados. Nessa trilha, ela não será de grande utilidade pois só utilizaremos arquivos de texto comuns, mas em projetos reais ela é muito útil para evitar que arquivos desnecessários sejam adicionados ao repositório.

## Instalação do Git

### Windows

1. Acesse o site a seguir e clique em Download: [https://git-scm.com/install/windows](https://git-scm.com/install/windows).
2. No geral, apenas siga as orientações de instalação, com algumas ressalvas:
   1. **Editor padrão**: como utilizaremos o VSCode como editor nessa trilha, é preferível selecionar a opção **Use Visual Studio Code as Git's default editor**, porém fica do seu critério.
   2. **Nome inicial da branch**: é recomendável selecionar a opção **Override the default branch name for new repositories** e deixa *main* como padrão, para evitar confusões futuras.
3. Após passar por todas etapas, clique em **Install** e aguarde a instalação ser concluída.
4. Se tudo deu certo, o Git já deve estar instalado no seu computador! Para verificar, abra o terminal e digite `git --version`. Se o terminal retornar a versão do Git instalada, isso significa que a instalação foi bem-sucedida.
5. Depois, é necessário uma configuração inicial do Git, para que ele saiba quem é você. Para isso, basta usar os seguintes comandos, substituindo as informações entre aspas pelas suas próprias informações:
   1. [`git config`](../guia_comandos/git_config.md) `--global user.name "Seu Nome"`
   2. [`git config`](../guia_comandos/git_config.md) `--global user.email "Seu Email"`
6. Pronto! Agora o Git está instalado e configurado no seu computador, e você pode começar a usar o controle de versão para seus projetos.

### Linux

1. Abra o terminal e use o seguinte comando para instalar o Git: `sudo apt install git -y`.
2. O Git já foi instalado (WOW)! Novamente, faremos a configuração inicial do Git com os mesmos comandos mencionados acima:
   1. [`git config`](../guia_comandos/git_config.md) `--global user.name "Seu Nome"`
   2. [`git config`](../guia_comandos/git_config.md) `--global user.email "Seu Email"`
3. Pronto! Instalado e configurado!


## Instalação do GitHub Desktop

### Windows 

1. Acesse o site a seguir e clique em Download: [https://desktop.github.com/download/](https://desktop.github.com/download/).
2. Para esse programa, não há literalmente nenhuma configração necessária durante a instalação
3. Nas telas de boas-vindas, faça o *sign in* com a sua conta do GitHub. Caso ainda não tenha uma, acesse [aqui](https://github.com/signup)
4. Na configuração de configuração do git, escolha a opção de "usar meu nome e email do GitHub", para que o GitHub Desktop possa usar as mesmas credenciais que você usa no GitHub.
5. Pronto! Agora o GitHub Desktop está instalado e configurado no seu Windows, e você pode começar a usar a interface gráfica para gerenciar seus repositórios de forma mais prática e intuitiva!

### Linux 

Nativamente, o GitHub Desktop não possui uma versão oficial para Linux. Porém, um programador incrível chamado [Brendan Forster](https://github.com/shiftkey) fez um belíssimo trabalho e fez um [fork](../glossario_conceitos/fork.md) do GitHub Desktop e adaptou para Linux! Portanto, segue abaixo o passo a passo:

1. Acesse o site a seguir, encontre a versão mais recente (ou a mais estável) e dentro de "Assets" escolha a versão .deb, .rpm ou .AppImage : [https://github.com/shiftkey/desktop/releases](https://github.com/shiftkey/desktop/releases)
2. Depois de baixar o arquivo, basta clicar duas vezes nele para iniciar a instalação, ou usar o terminal para instalar o pacote, dependendo da sua distribuição.
3. Nas telas de boas-vindas, faça o *sign in* com a sua conta do GitHub. Caso ainda não tenha uma, acesse [aqui](https://github.com/signup)
4. Configure o nome e email do GitHub Desktop, para que ele possa usar as mesmas credenciais que você usa no GitHub.
5. Pronto! Agora o GitHub Desktop está instalado e configurado no seu Linux!