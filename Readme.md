Olá, esse será o meu primeiro projeto aqui.
Através dele aprenderemos a utilizar o git!

----------------------------------------------------

Algumas informações iniciais importantes:

----------------------------------------------------

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

----------------------------------------------------------------------

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






