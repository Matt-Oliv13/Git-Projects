Olá, esse será o meu primeiro projeto aqui.
Através dele aprenderemos a utilizar o git!

----------------------------------------------------

Algumas informações iniciais importantes:

----------------------------------------------------

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

O comando 'git init' é o ponto de partida de qualquer repositório, sendo o comando responsável por transformar um diretório comum em um projeto monitorado pelo Git. Ao ser executado, ele inicializa um novo repositório através da criação de uma pasta oculta chamada .git, que funciona como o "cérebro" do projeto, armazenando todo o histórico de versões, metadados e configurações de controle. A partir desse momento, o Git cria automaticamente o branch principal (geralmente chamado de main ou master) e permite que você comece a registrar as mudanças nos arquivos. Sem esse comando, o terminal não reconhecerá outros comandos de versão dentro daquela pasta, pois é o git init que estabelece a infraestrutura necessária para o rastreamento de código.

----------------------------------------------------------------------


