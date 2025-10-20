# Sistema de Gerenciamento de Biblioteca Digital
Sistema eficiente para gestão de documentos da sua biblioteca digital.

1. DESCRIÇÃO
   
O script foi concebido como uma solução de desenvolvimento de software para otimizar a gestão da coleção digital de uma biblioteca universitária, abordando os desafios de um acervo em constante expansão. A biblioteca possui uma vasta coleção de documentos digitais, incluindo artigos, teses e livros em múltiplos formatos (PDF, ePUB, HTML, etc). Atualmente a organização desses arquivos é realizada de forma manual e, portanto, é um processo demorado e altamente suscetível a inconsistências. 

2. OBJETIVOS

O objetivo principal do script é automatizar e padronizar a catalogação de documentos digitais. Além disso, também busca reduzir o tempo gasto pela equipe em tarefas de arquivamento, minimizar erros humanos na classificação, melhorar a rastreabilidade e a facilidade de acesso aos documentos no acervo digital.

3. REQUISITOS

- Múltiplas Fontes: Ser capaz de processar arquivos vindos de duas fontes principais: uma pasta local no computador (upload pelo Desktop) e uma pasta designada no Google Drive.
- Lógica de Organização (Tipo de extensão): Ser capaz de identificar, classificar e salvar automaticamente cada documento em uma pasta correspondente ao seu tipo de arquivo (extensão).
- Lógica de Organização (Ano de publicação): Dentro de cada pasta de tipo de arquivo, Ser capaz de identificar o ano de publicação, lendo o nome do arquivo (ex: tese_2024.pdf seria classificado no ano 2024), classificar e salvar automaticamente cada documento em subpastas dentro de cada pasta de tipo de arquivo, baseadas no ano de publicação do documento. Na ausência de um ano no nome do arquivo, o script deveria atribuir o ano corrente (ex: 2025) como padrão.
- Interface de Usuário: Criar e configurar uma interface de linha de comando (CLI) simples e eficiente, para que a equipe da biblioteca possa operar o sistema sem conhecimento de programação. A interface deve permitir não apenas a organização de arquivos, mas também a adição, renomeação e remoção.

4. INSTRUÇÕES DE USO

O script opera através de um menu principal interativo (Interface de linha de comando). O usuário seleciona a ação desejada digitando o número correspondente e segue conforme as instruções do programa.

- Etapa 0: Inicialização > Ao executar o script pela primeira vez (no ambiente Google Colab), ele automaticamente cria as duas pastas principais necessárias para a operação:
"arquivos_para_organizar": Pasta local temporária para onde os arquivos enviados do computador irão.
"biblioteca_organizada": A pasta final onde toda a estrutura de arquivos classificados será armazenada.

- Etapa 1: Adicionar Arquivos > Antes de organizar, o usuário deve indicar ao script onde os arquivos a serem organizados estão localizados.
  
L> Digitar "1" no menu interativo = Opção 1: Usar uma pasta do Google Drive como origem
Descrição: Conecta o script à conta Google Drive do usuário e solicita o caminho para uma pasta específica. O script passará a considerar essa pasta do Drive como a fonte principal de arquivos.
Uso: Ideal para processar grandes lotes de arquivos que já estão armazenados na nuvem.

(OU)

L> Digitar "2" no menu interativo = Opção 2: Adicionar novos arquivos da pasta de origem.
Descrição: Permite fazer o upload de um ou mais arquivos diretamente da máquina local do usuário (Desktop do seu computador) para a pasta "arquivos_para_organizar" no ambiente Colab.
Uso: Ideal para adicionar poucos arquivos de cada vez.

- Etapa 2: Executar a Organização
  
L> Digitar "3" no menu interativo = Opção 3: Organizar arquivos da pasta de origem
Descrição: Esta é a função principal. O script analisa todos os arquivos na pasta de origem (seja a pasta local do Colab ou a pasta do Google Drive, definida na Etapa 1).
Processo: Para cada arquivo, ele identifica a extensão (ex: pdf) e o ano (ex: 2024 ou 2025-se nenhum for encontrado). Em seguida, ele move o arquivo para a pasta "biblioteca_organizada" correspondente (ex:bibliotexa_organizada/pdf/2024).

- Etapa 3: Gerenciamento de Arquivos > Após a organização, o script permite a manutenção do acervo.

L> Digitar "4" no menu interativo = Opção 4: Renomear um arquivo já organizado
Descrição: Solicita o nome exato do arquivo antigo e o novo nome a ser colocado. O script busca o arquivo em toda a estrutura da "biblioteca_organizada" e o renomeia em seu local atual.

(OU)

L> Digitar "5" no menu interativo = Opção 5: Remover um arquivo já organizado
Descrição: Solicita o nome exato do arquivo a ser excluído. O script o localiza dentro da "biblioteca_organizada" e o remove permanentemente.

- Etapa 4: Encerrar o Programa
  
L> Digitar "6" no menu interativo = Opção 6: Sair do programa
Descrição: Encerra o script de forma segura.

5. RESULTADOS E BENEFÍCIOS

A execução bem-sucedida do script transforma um conjunto desorganizado de arquivos em um acervo digital estruturado de forma lógica e padronizada. O resultado é a pasta "biblioteca_organizada" populada com uma hierarquia clara de tipo de arquivo (extensão) e ano de publicação. 

Além disso, possui uma *feature adicional de logging*. A execução do script também cria uma pasta chamada 'registros_log', em que são armazenados arquivos.txt, os quais contêm registros de cada nova interação com a interface CLI. Os registros informam qual ação do menu interativo foi solicitada, qual arquivo será afetado, data no momento da ação (em formato brasileiro) e horário no momento da ação (conforme fuso horário de Brasília). 

Os benefícios incluem:

- Eficiência Operacional: A automação da tarefa de classificação economiza horas de trabalho manual, liberando a equipe da biblioteca para atividades de maior valor.

- Consistência e Padronização: O sistema impõe uma regra de organização única e consistente, eliminando a variabilidade e os erros do arquivamento manual.

- Acessibilidade e Recuperação: A estrutura lógica (Tipo > Ano) torna a localização e recuperação de documentos digitais um processo rápido e intuitivo para toda a equipe.

- Escalabilidade: O sistema está preparado para lidar com o crescimento do acervo digital, processando milhares de documentos com a mesma eficiência de processar apenas um.

- Rastreabilidade e Segurança: Através da criação automática dos logs a cada interação na interface de comandos, é possível rastrear com facilidade e segurança o que foi feito, com qual arquivo e quando foi feito, dentro do Sistema de gerenciamento de arquivos digitais.

*# Para mais informações obre como pode contribuir com este e outros repositórios, acesse o arquivo 'CONTRIBUTING.md' deste repositório.*
