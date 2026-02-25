## • **Anotações de códigos do Git Bash**

#### » Ciclo de Vida/Estado dos Arquivos:

|Estado|Descrição|
|---|---|
|Untracked|Arquivos criados mas ainda não rastreados pelo Git. Use `git add` para começar a rastrear.|
|Unmodified|Arquivos rastreados, mas sem modificações.|
|Modified|Arquivos com modificações, mas ainda não adicionados à área de stage.|
|Staged|Arquivos prontos para serem comitados com `git commit`.|

---

#### » **Comandos para Modificação de Estágios:**

|Comando|Transição|Descrição|
|---|---|---|
|`git add`|Untracked → Staged|Começa a rastrear arquivos.|
|`git commit`|Staged → Unmodified|Salva o estado atual no log (commit).|
|`git commit -am "msg"`|Modified → Commit direto|Adiciona e comita de uma vez, apenas para arquivos já rastreados.|
 > **Nota: Sempre tenha em mente em manter os commits com mensagens simples e de fácil entendimento.

#### » **Comandos Git Bash:**

|Comando|Descrição|
|---|---|
|`git config user.name`|Define o nome do usuário do Git|
|`git config user.email`|Define o email do usuário|
|`git config init.defaultBranch`|Altera o nome da branch padrão (ex: main)|
|`mkdir <nome>`|Cria um diretório|
|`cd <nome>`|Entra em um diretório|
|`cd ..`|Volta um nível na navegação|
|`git init`|Inicia um repositório Git|
|`ls`|Lista os arquivos do diretório|
|`touch <arquivo.ext>`|Cria um novo arquivo|
|`pwd`|Mostra o diretório atual|
|`rm <arquivo>`|Remove o arquivo especificado|
|`rmdir <diretório>`|Remove o diretório especificado|
|`git diff`|Mostra as diferenças entre arquivos modificados|
|`git clone <URL>`|Clona um repositório remoto|
|`git remote -v`|Mostra as URLs dos repositórios remotos configurados|
|`git push -u origin <branch>`|Envia as alterações para o repositório remoto|
|`git checkout <arquivo>`|Descarta alterações no arquivo|
|`git checkout -b <nome>`|Cria uma nova branch e muda para ela|
|`git branch -m <novo>`|Renomeia a branch atual|
|`git branch`|Lista as branches locais|
|`git add .`|Adiciona todos os arquivos modificados/untracked à área de stage|
|`git checkout <branch>`|Muda para outra branch|
|`git merge <branch>`|Mescla a branch especificada com a branch atual|

---

####  » **Resets:**

| Comando                    | Efeito                                                          |
| -------------------------- | --------------------------------------------------------------- |
| `git reset`                | Retira arquivos da área de stage (volta ao estado modified)     |
| `git reset --soft <hash>`  | Volta para commit anterior, mantendo arquivos na área de stage  |
| `git reset --mixed <hash>` | Volta para commit anterior, removendo arquivos da área de stage |
| `git reset --hard <hash>`  | Volta para commit anterior e descarta todas as modificações     |

> **Nota:** _hash_ refere-se ao identificador único do commit que se deseja voltar.
