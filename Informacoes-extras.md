# Outros Comandos Importantes!

## Gerais 

Verifica se é um repositório Git e mostra o estado atual do seu repositório, informando mudanças desde o último commit e o que ocorrerá no próximo:

      git status

Lista arquivos, incluindo arquivos ocultos (como a pasta .git):

      ls -la

cd: 

      cd nomedapasta : Entrar na pasta

      cd .. : voltar

cat : muito usado simplesmente para exibir o conteúdo de arquivos.
      
      ex: cat .git/config : exibe o conteúdo do arquivo de configurações do repositório.
      
      ex: cat .git/logs/HEAD : exibe todas as movimentações do HEAD (commits, checkouts, merges etc.);

Exibe a url do repositório no GitHub:

      git remote -v

Exibe todas as configurações do git:
 
      git config --list

----------------------------------------------------------------------------------

## Branchs

O 'git checkout' serve para navegar entre diferentes versões do seu projeto. Para mudar de uma branch para outra, usamos: 
   
    git checkout nome-da-branch 

Se o objetivo for criar uma nova ramificação e já entrar nela, o comando é:
    
    git checkout -b nova-branch

Atualmente, o Git recomenda o uso do 'git switch' por ser mais específico para essa tarefa. 
    
    Para trocar de branch: git switch nome-da-branch
    Para criar uma nova branch: git switch -c nova-branch 

Ambos os comandos atualizam seus arquivos locais para a versão da branch escolhida. 

----------------------------------------------------------------------------------

## Clone

Clonar um repositório usando HTTPS:
  
     git clone link

Clonar um repositório usando SHH:
     
     git clone chave:usuario/repositorio.git

Clonar alterando o nome da pasta:

     git clone URL novo_nome

Clona o respositório, mas abre na branch específica:

     git clone --branch nome-da-branch URL    OU    git clone --b nome-da-branch URL

Clonar apenas a branch especificada sem as demais:

     git clone --branch nome-da-branch --single-branch URL

-----------------------------------------------------------------------------------

## .gitignore

O arquivo .gitignore é utilizado para informar ao Git quais arquivos ou pastas devem ser ignorados e, portanto, não serem adicionados ao controle de versão.

Criando o arquivo diretamente pelo git:
   
      touch .gitignore

Adicionando um arquivo ou pasta para ser ignorado:
      
      echo "arquivo.txt" >> .gitignore
      
      echo "pasta/" >> .gitignore

Removendo uma regra do .gitignore:
      
      nano .gitignore
      
      Apague a linha desejada, salve (Ctrl + O, Enter) e saia (Ctrl + X).

Verificando se está sendo ignorado:

      git status

Se o arquivo ou pasta não aparecer na saída (e ainda não estiver sendo rastreado pelo Git), significa que o .gitignore está funcionando corretamente.






