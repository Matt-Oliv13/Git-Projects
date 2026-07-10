PRIMEIROS PASSOS E CONCEITOS BÁSICOS

O Git é o sistema de controle de versão mais usado no mundo. Ele registra o histórico de alterações de códigos e arquivos, permitindo que você acompanhe a evolução do projeto, reverta modificações para estados anteriores e trabalhe em equipe sem sobrescrever o trabalho de outros.

Abra o arquivo/pasta com Git Bash
O Git Bash é um aplicativo de terminal para Windows. Ele emula o ambiente de linha de comando Linux/Unix e permite que você execute comandos Git no seu computador.

--------------------------------------------------------------------------------

Comandos iniciais pós-instalação

git config --list : ver todas as configurações
git config --global user.name : define o nome o usuário
git config --global user.email : define o email do usuário
OBS:
    --local   (somente este repositório)   ← maior prioridade
    --global  (somente seu usuário)
    --system  (todos os usuários do computador) ← menor prioridade // Normalmente é necessário executar o terminal como administrador para alterá-la. Esse nível é mais usado por administradores de sistemas ou em computadores compartilhados.
    
---------------------------------------------------------------------------------

Verificação de Caminho

O comando 'cd' (change directory) é a ferramenta de navegação do terminal. Ele altera o foco do sistema para uma pasta específica para que você possa executar comandos dentro dela. O 'cd' precisa de um Caminho (Path) para saber onde ir. 

-Caminho Relativo: Baseado na sua posição atual.
    Exemplo: cd imagens (Entra na pasta que está dentro da atual).
    Exemplo: cd .. (Sobe um nível, voltando para a pasta "pai").

-Caminho Absoluto: O endereço completo desde a raiz do computador.
    Exemplo (Windows): cd C:\Users\Nome\Desktop\Projeto.
    Exemplo (Mac/Linux): cd /Users/nome/projeto.

Dicas Práticas:
-Auto-completar: Digite as primeiras letras do nome da pasta e aperte Tab. Se o terminal preencher o resto, o caminho está correto.
-Arrastar e Soltar: Você pode digitar cd  (com espaço) e arrastar a pasta da sua área de trabalho diretamente para dentro do terminal. Ele escreverá o caminho completo para você.
-Localização Atual: Se estiver perdido, digite pwd no GitBash para ver o caminho completo de onde você está agora.

--------------------------------------------------------------------

Criando um Repositório

O comando 'git init' é o ponto de partida de qualquer repositório, sendo o comando responsável por transformar um diretório comum em um projeto monitorado pelo Git. Ao ser executado, ele inicializa um novo repositório através da criação de uma pasta oculta chamada .git, que funciona como o "cérebro" do projeto, armazenando todo o histórico de versões, metadados e configurações de controle. A partir desse momento, o Git cria automaticamente o branch principal (geralmente chamado de main ou master) e permite que você comece a registrar as mudanças nos arquivos. Sem esse comando, o terminal não reconhecerá outros comandos de versão dentro daquela pasta, pois é o git init que estabelece a infraestrutura necessária para o rastreamento de código.

---------------------------------------------------------------------------------

Branch

No Git, uma branch (ramo), funciona como uma linha do tempo alternativa e isolada do desenvolvimento principal. Ela permite criar novas funcionalidades ou corrigir bugs sem alterar o código estável da branch principal, geralmente chamada de main ou master. As branches facilitam o trabalho paralelo e a experimentação segura.

O comando 'git branch' é a ferramenta utilizada para gerenciar as diferentes linhas de desenvolvimento dentro de um repositório, permitindo que você crie, liste ou exclua ramificações do projeto original.
    
-Isolamento de Tarefas: Ao criar uma nova branch, você gera um ambiente isolado para trabalhar em uma demanda específica; após concluir e testar as alterações, essas linhas podem ser unificadas novamente ao tronco principal.
    
-Gerenciamento do Repositório: O comando permite visualizar todas as ramificações existentes (destacando com um asterisco aquela em que você está no momento), renomear ramos ou deletar aqueles que já cumpriram seu propósito e foram mesclados.

#Nota Importante: 
-Renomear a branch atual: Se você já estiver na branch que deseja renomear, basta digitar: git branch -m "novo-nome". O parâmetro -m vem de move (ou rename).
-Renomear outra branch: Caso você queira renomear uma branch na qual não está no momento, use: git branch -m "nome-antigo" "novo-nome".

Repositórios Remotos: Esse comando altera apenas o nome da branch no seu computador local. Se a branch já tiver sido enviada para um servidor (como GitHub ou GitLab), você precisará deletar a branch antiga no remoto e fazer o "push" da nova 

    >Renomeie localmente: git branch -m novo-nome 
    >Delete a antiga no remoto: git push origin --delete nome-antigo
    >Envie a nova e configure o rastreio: git push origin -u novo-nome.

---------------------------------------------------------------------------------

Staging Area ("Sala de espera local")

Ela serve para você selecionar, organizar e revisar quais arquivos modificados você deseja incluir no próximo "pacote" de alterações (o commit), funcionando como uma zona de preparação intermediária. Ela possibilita criar commits menores, lógicos e limpos, separando o rascunho de trabalho da versão final

Adicionando arquivos ao 'Staging Area'
O comando 'git add' é o responsável por preparar as modificações realizadas no seu diretório de trabalho para o próximo commit, funcionando como uma área de triagem técnica conhecida como Staging Area. Ao executar este comando, você sinaliza ao Git quais arquivos ou trechos de código devem ser incluídos na próxima "foto" do projeto, permitindo um controle granular sobre o que será registrado no histórico.
        
-Seleção Flexível: Você pode adicionar arquivos individualmente (git add arquivo.txt) ou incluir todas as alterações da pasta atual de uma vez utilizando o comando 'git add .'
        
-Estado Preparado: Após o comando, os arquivos passam do estado "modificado" para "preparado" (staged), ficando listados em verde no comando git status e prontos para serem oficializados pelo commit quando o desenvolvedor quiser.

----------------------------------------------------------------------------------

O Commit

O comando git commit funciona como a gravação oficial de um "ponto de restauração" no histórico do seu projeto, transformando as alterações preparadas na Staging Area em um registro permanente e imutável. Cada commit gera um identificador único (hash) e captura o estado exato de todos os arquivos naquele momento, permitindo que você navegue pelo tempo e recupere versões anteriores do código caso algo dê errado ou precise ser revisado no futuro.

-Identidade e Mensagem: Todo commit exige uma mensagem explicativa (através do parâmetro -m) e informações do autor, servindo como uma documentação viva sobre o porquê de cada mudança ter sido feita.

Formatação: git commit -m "mensagem"

-Snapshot Permanente: Diferente de um salvamento comum de arquivo, o commit não sobrescreve o anterior; ele empilha uma nova camada de histórico, criando uma linha do tempo segura para o desenvolvimento do software.

----------------------------------------------------------------------------------

Estabelecimento do vínculo com um Servidor

O comando git remote add origin https://...git serve para conectar o seu repositório local a um servidor na internet, criando um vínculo de comunicação entre o seu computador e o serviço de hospedagem (como o GitHub). Ao executá-lo, você está dizendo ao Git: "A partir de agora, o endereço oficial na nuvem para este projeto será esta URL, e eu vou chamá-la pelo apelido de origin".

-Criação do Atalho: Em vez de digitar a URL completa sempre que quiser enviar código, você passa a usar apenas o nome origin. Ele funciona como um contato salvo na agenda do seu celular: você clica no nome para não precisar decorar o número.
    
-Preparação para o Envio: Este comando é uma configuração única; ele não envia seus arquivos imediatamente, mas estabelece o caminho necessário para que o comando git push saiba exatamente para onde despachar suas alterações.

----------------------------------------------------------------------------------

Push e Pull

O comando git push serve para "empurrar" ou enviar as suas alterações locais para o servidor remoto. Depois que você terminou uma tarefa, salvou as mudanças e fez o commit (ponto de restauração), você usa o push para disponibilizar essas atualizações para o restante da equipe. 

-Envie ao servidor:
    (a) Pela primeira vez: git push -u origin main (isso conecta sua pasta local ao servidor). Atenção! 'main' é o nome padrão da Branch que utilizaremos.
    (b) Nas próximas vezes: Apenas 'git push origin main' ou 'git push'

OBS: O parâmetro -u (abreviação de --set-upstream) cria um vínculo de rastreamento entre a branch local main e a branch main no repositório remoto origin.Vantagem: Após executá-lo uma primeira vez, o Git "lembra" para onde essa branch deve ir. Nas próximas vezes, você poderá usar apenas git push ou git pull sem precisar especificar o nome do remoto ou da branch.

Já o comando git pull funciona como um "puxar" ou atualizar o seu projeto. Quando você trabalha em equipe ou de diferentes computadores, outras pessoas podem ter enviado alterações para o servidor. Ao executar o pull, o Git busca essas novidades na nuvem e as traz para a sua máquina, tentando mesclá-las (fazer o merge) automaticamente com o que você já tem. É a maneira de garantir que você está trabalhando na versão mais recente do código e evitar conflitos no futuro.

-Receba do servidor:
    (a) git pull origin main;
    (b) ou apenas git pull (se você não trabalha com mais de um repositório)

Em resumo, enquanto o pull mantém você atualizado com o que os outros fizeram, o push atualiza o mundo com o que você criou.

----------------------------------------------------------------------------------

Juntando branchs

Uma vez posicionado na branch de destino, execute o comando: 
    git merge nome-da-branch-origem
    
OBS: "origem" é a branch que contém as novas funcionalidades ou correções a serem unidas. Nesse momento, o Git tentará unir as histórias de commit de forma automática, podendo haver dois cenários possíveis:
    (a) a branch de destino não recebeu commits após a criação da branchde origem, permitindo que o Git apenas mescle as duas. 
    (b) a branch de destino e a de origem evoluíram independentemente, exigindo que o Git crie um novo "commit de merge" para selar a união. Caso o Git encontre alterações conflitantes no mesmo trecho de um arquivo, o merge será pausado e você entrará em um estado de conflito. Nessa situação, é necessário abrir os arquivos sinalizados, escolher manualmente qual versão do código deve permanecer, salvar e marcar o conflito como resolvido com git add. Por fim, basta concluir a integração com um git commit (caso o Git não tenha feito automaticamente) e, se desejar que essas mudanças apareçam no servidor, realizar o git push. Após o sucesso da operação, é comum deletar a branch de origem para manter o repositório organizado.

---------------------------------------------------------------------------------

