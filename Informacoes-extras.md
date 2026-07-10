Outros Comandos Importantes!

git status : verifica se a pasta é um repositório Git;

ls -la : Lista arquivos, incluindo arquivos ocultos (como a pasta .git);

cd nomedapasta : Entrar na pasta
cd .. : voltar

cat : muito usado simplesmente para exibir o conteúdo de arquivos.
ex: cat .git/config : exibe o conteúdo do arquivo de configurações do repositório.
ex: cat .git/logs/HEAD : exibe todas as movimentações do HEAD (commits, checkouts, merges etc.);

git remote -v : exibe a url do repositório no GitHub

git config --list : exibe todas as configurações do git

----------------------------------------------------------------------------------

* BRANCHS

O 'git checkout' serve para navegar entre diferentes versões do seu projeto. Para mudar de uma branch para outra, usamos: 
   
    git checkout nome-da-branch 

Se o objetivo for criar uma nova ramificação e já entrar nela, o comando é:
    
    git checkout -b nova-branch

Atualmente, o Git recomenda o uso do 'git switch' por ser mais específico para essa tarefa. 
    
    Para trocar de branch: git switch nome-da-branch
    Para criar uma nova branch: git switch -c nova-branch 

Ambos os comandos atualizam seus arquivos locais para a versão da branch escolhida. 

----------------------------------------------------------------------------------

* CLONE
  
git clone link : clona um repositório usando HTTPS;

git clone chave:usuario/repositorio.git : clona um repositório usando SHH;

git clone URL novo_nome : clonar alterando o nome da pasta;

git clone --branch nome-da-branch URL    OU    git clone --b nome-da-branch URL : clona o respositório, mas abre na branch específica;

git clone --branch nome-da-branch --single-branch URL : clona apenas a branch especificada sem as demais;






