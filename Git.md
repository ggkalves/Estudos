![Git Study Header (1)](https://user-images.githubusercontent.com/124086216/221045132-16e8a662-d58c-42c9-97c3-c6fec965732c.png)

<br>

# Oque é Git?
Git é um sistema de controle de versão (VCS) desenvolvido por Linus Torvalds (o criador do Linux).
Utilizado nos dias de hoje por muitas empresas, foi tomando espaço dos outros sistemas de controle que acabaram por se tornarem ultrapassados, e passou a ser o padrão mundial para controle de versão atualmente acomodando mais de 25 milhões de usuários.

É um serviço baseado em nuvem que hospeda um sistema de controle de versão (VCS). 
Permitindo que os desenvolvedores colaborem e façam mudanças em projetos compartilhados enquanto mantêm um registro detalhado do seu progresso.

<h2>Sistema de controle de versão (VCS) </h2>

Sempre que desenvolvedores criam um novo projeto, é normal que com o tempo surjam novas atualizações do código base como correções de buhs, adição de novas ferramentas, ajustes
que o cliente pode pedir futuramente, etc. Isso até mesmo depois do lançamento oficial, por isso ocorrem as atualizações de versões. E o sistema de controle de versão ajuda
a acompanhar as mudanças feitas no código além de registrar quem efeuou a mudança e permite também a restauração de um código removido ou modificado.

# Os conceitos do Git

Antes de tudo é importante entender os conceitos do Git, a primeiro momento pode assustar, mas a compreensão de pelo menos os principais conceitos dessa ferramenta
pode facilitar passar por obstáculos característicos dos primeiros momentos em que manipulamos algo novo.

Os principais conceitos do Git são:

- Repositório: É o local onde as alterações em um projeto são armazenadas. Pode ser local (no computador do desenvolvedor) ou remoto (em servidores como o GitHub, GitLab ou Bitbucket).

- Commit: É uma unidade básica de mudança em um repositório Git. Representa uma versão específica do projeto, incluindo todas as alterações feitas desde o último commit.

- Branch (ramificação): É uma ramificação independente do projeto em um repositório. É útil para trabalhar em novas funcionalidades ou corrigir bugs sem afetar a versão principal (branch master ou main) do projeto.

- Merge (mesclar): É o processo de combinar alterações de uma branch em outra, geralmente fundindo as mudanças de uma branch secundária na branch principal.

- Pull Request (solicitação de pull): É uma solicitação feita por um desenvolvedor para mesclar suas alterações em uma branch secundária com a branch principal de um repositório. É comumente usado em fluxos de trabalho de colaboração em equipe.

- Clone (clonar): É o processo de criar uma cópia local de um repositório remoto em um computador local.

- Push (enviar): É o processo de enviar alterações feitas localmente para um repositório remoto.

- Pull (receber): É o processo de obter as atualizações mais recentes de um repositório remoto e aplicá-las em um repositório local.

Esses conceitos são fundamentais para entender como o Git funciona e como utilizar suas funcionalidades para gerenciar as mudanças em projetos de software de forma eficiente e colaborativa.

<h2> Repositórios </h2>

Os repositórios são os ambientes criados para armazenar códigos.

Você pode possuir um ou mais repositórios, públicos ou privados, locais ou remotos, e eles podem armazenar não somente os próprios códigos a serem modificados, mas também imagens, áudios, arquivos e outros elementos relacionados ao seu projeto.

É através dos seus repositórios públicos que outros programadores poderão ter acesso aos seus códigos no GitHub, podendo, inclusive, cloná-los para adicionar melhorias.


Os repositórios são a base do Git e são onde todas as mudanças em um projeto são armazenadas. Um repositório pode ser local, ou seja, estar no computador do desenvolvedor, ou remoto, hospedado em um servidor como o GitHub, GitLab ou Bitbucket.

<h3>Repositório Local </h3>

Um repositório local é uma pasta em seu computador que contém todos os arquivos e histórico de um projeto Git. É possível criar um novo repositório Git em um diretório existente de seu computador ou iniciar um novo projeto com um repositório vazio.

Para criar um novo repositório Git em um diretório existente, basta abrir o terminal na pasta do projeto e executar o comando:

`$ git init$`

Isso inicializará um novo repositório Git no diretório atual, criando uma pasta oculta chamada ".git" que conterá todos os metadados e informações de controle de versão.

<h3>Repositório Remoto</h3>

Um repositório remoto é um local na nuvem onde os arquivos de um projeto Git são armazenados. Ele pode ser acessado por vários desenvolvedores para colaborar em um projeto em equipe.

Os repositórios remotos são populares para colaboração, compartilhamento de código e implantação de projetos. Existem várias plataformas de hospedagem de repositórios Git, como GitHub, GitLab, Bitbucket, entre outras.

Para adicionar um repositório remoto a um repositório local, é possível utilizar o comando:

`$ git remote add origin <URL do repositório remoto>`

Isso permite que você faça push (enviar) e pull (receber) de alterações para e do repositório remoto.

<h3>Trabalhando com Repositórios</h3>

Uma vez que um repositório Git tenha sido criado, é possível realizar uma série de operações, como:

- Commit: Criar uma nova versão do projeto com as alterações realizadas.
- Branch (ramificação): Criar ramificações independentes do projeto para trabalhar em funcionalidades ou correções sem afetar a versão principal.
- Merge (mesclar): Combinar alterações de uma branch em outra, geralmente fundindo as mudanças de uma branch secundária na branch principal.
- Pull Request (solicitação de pull): Solicitar a mesclagem de alterações de uma branch secundária em uma branch principal em um repositório remoto.
- Push (enviar): Enviar as alterações realizadas localmente para um repositório remoto.
- Pull (receber): Obter as atualizações mais recentes de um repositório remoto e aplicá-las em um repositório local.

Os repositórios são essenciais para o uso eficiente do Git e para colaboração em equipe, permitindo o controle de versão de um projeto, o gerenciamento de mudanças e o compartilhamento de código entre desenvolvedores.


<h2>Commit (Confirmação)</h2>

No Git, um commit é uma ação de salvar alterações feitas em um repositório. É uma forma de registrar permanentemente as mudanças feitas nos arquivos do projeto e criar um ponto de referência que pode ser revisitado posteriormente.

Os commits são usados para rastrear o histórico de alterações em um repositório Git, permitindo que os desenvolvedores revisem, comparem e voltem a versões anteriores do projeto. Os commits são atômicos, o que significa que cada commit registra apenas uma alteração específica no projeto.

<h3>Criando um Commit</h3>
Para criar um commit, é necessário adicionar as alterações feitas nos arquivos do projeto ao índice (staging area) do Git e, em seguida, executar o comando de commit. O índice é uma área intermediária onde as mudanças são preparadas antes de serem efetivamente registradas em um commit.

O seguinte comando cria um commit com uma mensagem de confirmação:


`$ git add <nome_do_arquivo>`
# Adiciona as alterações ao índice
`$ git commit -m "Mensagem de confirmação"`
# Cria um commit com a mensagem de confirmação

É importante fornecer uma mensagem de confirmação significativa que descreva brevemente as alterações feitas no commit.

<h3>Visualizando Commits</h3>

É possível visualizar os commits existentes em um repositório Git usando o seguinte comando:

`$ git log`

Isso exibirá uma lista dos commits em ordem cronológica inversa, mostrando informações como o hash do commit, autor, data e mensagem de confirmação.

<h3>Revisando Commits</h3>
Os commits permitem revisar e comparar alterações feitas em diferentes momentos do projeto. É possível visualizar as diferenças entre dois commits usando o seguinte comando:

`$ git diff <hash_do_commit1> <hash_do_commit2>`

Isso mostrará as diferenças entre os arquivos nos dois commits especificados.

<h3>Desfazendo Commits</h3>
É possível desfazer commits anteriores usando o comando git reset. É importante ter cuidado ao desfazer commits, pois isso pode resultar na perda permanente de alterações. Para desfazer o commit mais recente, pode-se usar o seguinte comando:


`$ git reset HEAD~1`

Isso desfaz o commit mais recente, mantendo as alterações feitas nos arquivos do projeto.

Os commits são uma parte fundamental do fluxo de trabalho do Git, permitindo que as alterações sejam registradas e rastreadas ao longo do tempo. É importante criar commits significativos e entender como revisar e desfazer commits corretamente para gerenciar eficientemente o histórico de alterações em um repositório Git.


<h2>Branch (Ramificação)</h2>

O conceito de branch (ou ramificação) é fundamental no Git, permitindo que os desenvolvedores trabalhem em diferentes versões independentes de um projeto em paralelo. Uma branch é basicamente uma cópia do repositório em um estado específico, permitindo que as alterações sejam feitas isoladamente sem afetar a versão principal do projeto.

As branches são usadas para várias finalidades, como desenvolvimento de novas funcionalidades, correção de bugs, experimentação de ideias e manutenção de diferentes versões do projeto. As branches podem ser criadas, modificadas e mescladas no Git, oferecendo um fluxo de trabalho flexível e colaborativo.

<h3>Branch Principal</h3>

A branch principal em um repositório Git é geralmente chamada de "master" ou "main". Ela é considerada a versão estável do projeto e é usada como referência para outras branches. É importante garantir que a branch principal esteja sempre em um estado funcional e livre de erros.

<h3>Criando uma Branch</h3>
É possível criar uma nova branch a partir de uma branch existente. Para criar uma nova branch, pode-se utilizar o seguinte comando:


`$ git checkout -b <nome_da_branch>`
Isso cria uma nova branch com o nome especificado e muda o Git para a nova branch, permitindo que as alterações sejam feitas isoladamente nessa nova branch.

<h3>Trabalhando em uma Branch</h3>
Uma vez que uma nova branch tenha sido criada, é possível fazer commit, modificar e adicionar arquivos no diretório de trabalho como de costume. Todas as alterações feitas serão isoladas na branch atual e não afetarão a branch principal ou outras branches.

<h3>Mesclando uma Branch</h3>
Quando as alterações em uma branch estiverem prontas para serem incorporadas à branch principal ou a outra branch, é possível mesclá-las. A mesclagem (merge) é o processo de combinar as alterações de uma branch em outra.

Para mesclar as alterações de uma branch em outra, pode-se utilizar o seguinte comando:

`$ git merge <nome_da_branch`

Isso incorporará as alterações da branch especificada na branch atual. É importante resolver quaisquer conflitos de mesclagem que possam ocorrer durante esse processo.

<h3> Gerenciando Branches </h3>
É possível listar, visualizar, renomear e excluir branches no Git. 
Alguns comandos úteis para gerenciar branches são:

- Listar branches existentes: `$ git branch`
- Mudar para uma branch específica: `$ git checkout <nome_da_branch>`
- Renomear uma branch: `$ git branch -m <nome_antigo> <nome_novo>`
- Excluir uma branch: `$ git branch -d <nome_da_branch>`

Lembrando que as branches são uma poderosa ferramenta do Git que permitem o trabalho paralelo em diferentes versões de um projeto, facilitando o desenvolvimento em equipe e o gerenciamento de mudanças. É importante compreender e utilizar corretamente as branches para garantir um fluxo de trabalho eficiente e organizado.

