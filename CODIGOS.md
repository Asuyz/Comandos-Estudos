**Anotações de codigos do Git Bash, para consulta ou estudo**

*clico de vida/estado dos arquivos*

-Untracked (Não rastreados)
-Arquivos criados mas que ainda não são rastreados pelo git, para começar o rastreio (-git add)

-Unmodified (sem modificações)
-Arquivos rastreados pelo git mas ainda sem alterações

-Modified (modificado)
-Arquivos modificados (com alterações) mas não enviados para a área de stage 

-Staged (preparado)
-arquivos prontos para serem comitados (-git commit)

*Comandos para modificação de estagios de arquivo*
-Git Add (De Untracked para Unmodified)> use esse comando para começar a rastrear o arquivo.
é possivel dar o add mais o commit com git -am "mensagem para o log"

-Git commit (De Staged para Unmodified)> Use esse comando para salvar o estado atual do arquivo (salvar alterações no log) 

*Comandos para o git bash*
-Git Config (os mais usados)

user.name + Usuario do git

user.email + Email do usuario

init.defaultBranch (Para mudar a Branch, a mais "padrão" sendo a main

-mkdir - para fazer um diretorio (pasta)

-cd (nome do diretorio/pasta) - para navegar no terminal

-cd (..) - para voltar um nivel de navegação 

-git init - iniciar um repositorio 

-ls - listar o contéudo do diretorio

-touch (mais a terminação do arquivo) - para criar um arquivo dentro do diretorio

-pwd - grava o diretorio sendo trabalhado no momento

-rm (mais o nome do arquivo) - remove o arquivo mencionado

-rmdir (mais o nome do diretorio) - remove o diretorio mencionado

-git diff - para visualizar as mudanças feitas no arquivo (comparar)

-git clone (mais a url) - para trazer o repositorio da nuvem

-git remote -v - verifica a url para realizar push ou fetch

-git push -u (origem e branch) - para upload no github

-git checkout (nome do arquivo) - para voltar as alterações do ultimo estagio salvo do arquivo trabalhado

-git checkout -b - cria uma nova Branch

-git checkout (mais o nome da branch) - para navegação entre as branchs

-git merge - junta os arquivos de diferentes branchs na branch em que você está no momento (ex: Juntar os arquivos da branch1 e branch2 para main)

*Resets*

-git reset - volta o arquivo de ser mandado para o Staged

-git reset --soft (hash) - volta o commit, porém mantem os arquivos prontos para commit

-git reset --mixed (hash) - volta o commit, porém os arquivos saem da área de staged 

-git reset ---hard (hash) - volta o commit e exclui todas as alterações
*Hash é o commit que queremos retornar*
