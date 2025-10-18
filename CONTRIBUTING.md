**MANEIRAS DE CONTRIBUIR**

________________________

A contribuição de outras pessoas em repositórios do GitHub é um pilar fundamental do ecossistema de desenvolvimento moderno, especialmente no mundo do código aberto. Ela transcende a simples adição de código, representando um processo vital de colaboração que impulsiona a qualidade, a inovação e a segurança. Através do fluxo contínuo de revisão por pares (code review) e esforço coletivo, a evolução do software é acelerada, construindo uma comunidade robusta em torno do projeto e garantindo sua sustentabilidade e relevância a longo prazo. A seguir detalho as 5 principais maneiras de contribuir com este e outros repositórios do GitHub, tanto através do Terminal de Comando (CLI) quanto via GitHub Desktop (GUI).

*1. Clonar um Repositório (Clone)*
   
Descrição: "Clonar" é o processo de criar uma cópia local exata de um repositório remoto (hospedado no GitHub) em sua máquina. Esta cópia inclui todos os arquivos, pastas, o histórico completo de alterações (commits) e todas as ramificações (branches) do projeto.

Objetivos:  Obter uma cópia de trabalho completa do projeto. Deve ser realizado para poder ler o código, fazer suas próprias alterações, testar e, eventualmente, contribuir de volta para o projeto original.

Como Fazer:

- Via Terminal (CLI)

1) No GitHub, copie a URL 'HTTPS' ou SSH do repositório (no botão "Code" do respositório que deseja clonar).
2) Abra seu terminal de comando do Git Bash, navegue até a pasta onde deseja salvar o projeto.
3) Execute o comando git clone seguido da URL > 'git clone https://github.com/nome-do-usuario/nome-do-repositorio.git'
   
- Via GitHub Desktop (GUI)

1) Abra o GitHub Desktop. Vá em "File" > "Clone Repository..." (ou Ctrl+Shift+O).
2) A aplicação mostrará uma lista dos seus repositórios no GitHub. Você pode selecionar um da lista, ou clicar na aba "URL" e colar a mesma URL usada no terminal.
3) Escolha o caminho local (onde salvar) e clique em "Clone".

___
*2. Criar uma nova ramificação (Branch)*

Descrição e Explicação: Uma "branch" (ramificação) é uma linha de desenvolvimento independente. Quando você cria uma nova branch, você está criando uma cópia do estado atual/principal do projeto (geralmente da branch main) onde pode trabalhar com segurança em uma nova funcionalidade ou correção de bug.

Objetivos: Isolação do main branch. Permite que você desenvolva e teste seu novo código sem afetar a branch principal (main), que deve ser mantida sempre estável e funcional. Isso é crucial para o trabalho em equipe e para organizar o processo de revisão de código. *Como regra de ouro, nunca faça alterações diretamente na main branch.* Crie uma nova branch para qualquer tarefa, por menor que seja (ex: feature/adicionar-login ou fix/corrigir-bug-layout).

Como Fazer:

- Via Terminal (CLI)

1) Certifique-se de estar na branch da qual deseja partir (ex: git checkout main).
2) No Bash, use o comando checkout com a flag -b (que significa "criar e mudar para"): 'git checkout -b nome-da-nova-branch'.
    
- Via GitHub Desktop (GUI)

1) No topo da aplicação, clique no botão "Current Branch" (que mostrará a branch em que você está, ex: main).
2) No menu que se abre, clique no botão "New Branch".
3) Digite o nome da sua nova branch (ex: feature/adicionar-login) e clique em "Create Branch". O aplicativo automaticamente mudará você para essa nova branch.

___
*3. Usar a bifurcação (Fork)*
   
Descrição e Explicação: Um "fork" não é um comando Git, mas uma ação específica da plataforma GitHub. Fazer um fork é criar uma cópia completa de um repositório (que pertence a outra pessoa ou organização) para a sua própria conta no GitHub. Este "fork" torna-se um repositório seu, sobre o qual você tem controle total.

Objetivos: Contribuir com projetos de código aberto (open source) que não lhe pertence. Como você não tem permissão para enviar alterações (push) diretamente para o repositório original, você faz um "fork" dele, envia as alterações para o seu fork e, em seguida, propõe que o mantenedor original aceite suas mudanças através de um Pull Request.

Como Fazer:

- Via Terminal (CLI)

1) Ação Prévia: O fork em si é feito na web. Vá à página do repositório no GitHub e clique no botão "Fork" no canto superior direito.
2) Ação no Terminal: Agora que você tem o fork na sua conta GitHub, você deve clonar o seu fork (não o original) para a sua máquina, usando o processo da Etapa 1.
3) No Bash, use 'git clone https://github.com/SEU-USUARIO/nome-do-repositorio-forkado.git'
   
- Via GitHub Desktop (GUI)

1) Ação Prévia: Assim como no terminal, clique no botão "Fork" no site do GitHub primeiro.
2) Ação no App: Após o fork ser criado, ele aparecerá na sua lista de repositórios. No GitHub Desktop, vá em "File" > "Clone Repository..." e selecione o repositório "forkado" da sua lista pessoal para clonar e depois alterar.

_______
*4. Fazer e comunicar alterações (Commits)*
   
Descrição e Explicação: Um "commit" é um "ponto de salvamento" (snapshot) no histórico do seu projeto. É um pacote de alterações que você fez nos arquivos. O processo envolve duas etapas: "Staging" (selecionar quais mudanças você quer salvar) e "Commit" (salvar essas mudanças com uma mensagem descritiva).

Objetivos: Criar um histórico lógico e rastreável das mudanças. Se algo quebrar, você pode ver quais alterações exatas causaram o problema e reverter. As mensagens de commit explicam o que e por que cada mudança foi feita, devendo ser feito frequentemente. Um commit deve representar uma unidade lógica de trabalho (ex: "Adiciona função de login", "Corrige erro de digitação no rodapé").

Como Fazer:

- Via Terminal (CLI)

1) Stage: Adicione os arquivos que você modificou à "área de preparação". No Bash, use 'git add arquivo-modificado.py'.
2) Ainda no Bash, use 'git add .' para adicionar TODAS as mudanças atuais realizadas.
3) Ainda no Bash, realize o commit e salve as mudanças preparadas com uma mensagem. Use 'git commit -m "Mensagem clara descrevendo a mudança"'.
   
- Via GitHub Desktop (GUI)

1) Stage: O app mostra todas as suas mudanças na aba "Changes". Marque a caixa de seleção ao lado dos arquivos (ou de linhas específicas dentro dos arquivos) que você deseja incluir no commit.
2) Commit: No canto inferior esquerdo, digite uma mensagem no campo "Summary" (obrigatório).
3) Clique no botão azul "Commit to <nome-da-branch>". O GitHub Desktop faz o "stage" e o "commit" em uma única ação.

___________
*5. Fazer e Aceitar Pull Requests (PR)*
   
Descrição e Explicação: Um "Pull Request" (PR) é um pedido formal para que o mantenedor de um repositório "puxe" (merge) as alterações de uma branch sua (que pode estar no seu fork ou no próprio repositório) para outra branch (geralmente a main). É o fórum central para a revisão de código (code review).

Objetivos: O PR é o coração da colaboração. Ele permite que outros desenvolvedores revisem seu código, façam comentários e sugiram melhorias antes que ele seja integrado ao código principal. Isso garante a qualidade, a padronização e a detecção precoce de bugs. Você cria um PR assim que sua funcionalidade ou correção (feita na SUA branch) estiver concluída, testada e pronta para ser discutida e integrada.

Como Fazer e Aceitar:

- Via Terminal (CLI)

1) Enviar o Código (Push): Primeiro, envie sua branch com seus commits para o repositório remoto (GitHub). No Bash, use 'git push origin nome-da-sua-branch'.
2) Criar o PR: O terminal não cria o PR diretamente. Ao fazer o push, o GitHub geralmente fornece um link no terminal que você pode copiar e colar no navegador para abrir a página de criação do PR.
3) Aceitar o PR: A aceitação (merge) não é feita pelo terminal (com Git puro). Ela é uma ação realizada pelo mantenedor do projeto na interface web do GitHub, clicando no botão "Merge pull request".

- Via GitHub Desktop (GUI)

1) Enviar o Código (Push): Após fazer seus commits, o aplicativo mostrará um botão "Push origin" (ou "Publish branch" se for a primeira vez). Clique nele.
2) Criar o PR: Assim que o "push" é concluído, o GitHub Desktop exibe uma nova seção com um botão "Create Pull Request". Clicar nele abrirá o navegador na página de criação do PR, já com as branches corretas selecionadas.
3) Aceitar o PR: Assim como no fluxo do terminal, a aceitação do PR é feita pelo mantenedor através da interface web do GitHub.
