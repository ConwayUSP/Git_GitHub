# Por Trás dos Panos

Nesse capítulo, iremos entender melhor como que toda essa mágica acontece: como que diferentes versões de um mesmo projeto coexistem na mesma máquina? Como que o Git consegue acompanhar as mudanças e identificar quem fez o quê? E como que o GitHub consegue hospedar repositórios e facilitar a colaboração entre desenvolvedores?

Geralmente, entender como as coisas funcionam por trás dos panos é uma ótima maneira de aprender a usar uma ferramenta de maneira mais eficiente e de uma forma mais intuitiva. Porém, se você não tem interesse em entender os detalhes técnicos do funcionamento do Git e do GitHub, pode pular para o próximo capítulo sobre [Criando um Repositório](./02_criando_repositorio.md).

## Sistemas de Controle de Versionamento 

Primeiro de tudo, vamos começar com o problema que o Git busca resolver. Imagine que você é um _web designer_, um escritor, até mesmo um desenvolvedor de software, seu trabalho atual é composto de vários arquivos que você vai editando e salvando conforme o trabalho avança. Mas chega a um ponto em que você quer experimentar uma nova funcionalidade ou um capítulo que você não tem certeza se vai para a versão final, para não perder o estado atual do seu projeto, você faz uma cópia dele em uma pasta diferente chamada "Projeto - Experimento 1". Ao finalizar esse experimento você começa a mexer mais no eu projeto até que ele esteja pronto, então você renomeia a pasta para "Projeto - Versão Final". Contudo, um _bug_ aparece, ou o seu revisor/supervisor encontra um problema e manda você consertar, você cria uma nova cópia chamada "Projeto - Versão Final 2". O que você está fazendo é, essencialmente, criar diversas **versões** (cópias) do seu trabalho, manualmente. Esse método pode levar a diversos erros, por exemplo, e se você apagar a versão errada? Ou atualizar uma versão desatualizada acidentalmente?

Para resolver esse tipo de problema os desenvolvedores &mdash; que também sofriam com esses males &mdash; criaram os **Sistemas de Controle de Versionamento** (VCS), um software que oferecia um jeito de controlar essas cópias, que permitiam reverter mudanças, combinar versões, ver quem foi o autor de certas mudanças, etc. Esses sistemas mantinham cópias dos arquivos e um registro da linha do tempo, bem como, alguns permitiam a colaboração remota entre autores.

## A História do Git

O Git surge dentro do _Kernel Linux_, após desavenças com o VCS proprietário BitKeeper, em que a permissão de uso comunitário foi revogada, o Linus Torvald (sim, O Linus Torvald) decidiu criar um sistema de versionamento que fosse:
- rápido
- simples
- voltado ao desenvolvimento não-linear (foco em versões paralelas)
- distribuído
- capaz de suportar projetos enormes (como o Kernel do Linux)

> _Fun Fact_: De acordo com Linus Torvald, _Git_ pode significar várias coisas dependendo do seu humor:
> 1. três letrar aleatórias, que formam um nome que não era usado por nenhum comando do Unix
> 2. Estúpido. Desprezível (_Dispicable_/_Contemptible_). Simples. Escolha uma palavra do dicionário.
> 3. "Global Information Tracker": quando tudo funcionar.
> 4. "Goddamn idiotic truckload of sh*t": quando alguma coisa der errado.

## Como o Git funciona?

A principal diferença entre o Git e o VCS que vieram antes deles é a forma como eles veem os dados. Os controles de versionamento geralmente guardam informações como uma lista de alterações nos arquivos ou guardam os arquivos e as alterações feitas. Porém, o Git vê como um _stream_ ou fluxo de _snapshots_ (fotos/capturas), ou seja, o Git tira uma "foto" de como os seus arquivos estão em dado momento e guarda uma referência para essa foto, mas se um arquivo não sofreu alterações o Git apenas usa a referência da foto anterior, isso evita uma quantidade enorme de redundância, com isso Git pode versionar projetos enormes com um custo baixo.

Desse modo, graças a técnica de "fluxo de imagens" do Git, ele pode funcionar quase como um _sistema de arquivos_ e é o que permite o sistema de [branches](../glossario_conceitos/branch.md) funcione tão bem. Além disso, o Git tem vários outros benefícios:
- **Localidade**: como o Git funciona majoritariamente no seu computador, você não tem que se preocupar de estar sem internet para editar o seu projeto. O mesmo não ocorria em VCS que dependiam da internet para funcionar.
- **Integridade**: o Git usa uma função de _checksum_ para codificar e referênciar seus itens, então não tem como mudar o histórico sem que o Git detecte isso.
- **Reversibilidade**: geralmente as operações do Git apenas incrementam dados armazenados, então é possível reverter quase todas as operações do Git, isso também torna bem difícil perder alguma coisa, se você salvou no histórico.

### Os três Estados do Git

Finalmente, para entender o fluxo de desenvolvimento dentro do Git, temos que entender que um arquivo pode estar sempre em um de **três estados**:
- [Modificado](../glossario_conceitos/working_directory.md): arquivo foi **modificado** mas não foi inserido no banco de dados.
- [Staged](../glossario_conceitos/staging_area.md): arquivo foi marcado e essa versão será enviado para o banco na próxima "snapshot".
- [Commited](../glossario_conceitos/commit.md): o arquivo está salvo no banco de dados.

Dessa forma, um projeto pode ter três seções: [Working Directory](../glossario_conceitos/working_directory.md), [Staging Area](../glossario_conceitos/staging_area.md), [Repository](../glossario_conceitos/repositorio.md), para os seus respectivos estados.

<img width="1203" height="663" alt="image" src="https://github.com/user-attachments/assets/1745752c-2482-4391-a1f5-1472beed5c78" />
Git Book. Capítulo 1.3 - "O que é o Git?".

Sendo assim, desenvolver com o Git é seguir o seguinte fluxo:
1. Modificar arquivos
2. Selecionar os arquivos que você quer salvar no seu próximo "commit", como _staged_.
3. Commitar, salvando esses arquivos no banco de dados do Git
4. Repetir etapa 1.

Com isso em mente, os próximos capítulos vão te ensinar a usar o Git e o Github para desenvolver projetos.
