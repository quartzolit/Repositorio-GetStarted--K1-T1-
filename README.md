# Repositorio-GetStarted--K1-T1-

Listando brevemente alguns comandos aprendidos no curso do Git

## Git Status
Verifica se todos os arquivos do repositório estão de acordo com a última versão de commit

## Git ADD

Realiza o reconhecimento de mudanças feitos no repositório local. Seja a criação de um arquivo novo ou a modificação de um arquivo existente.

        git add . 
        git add --all
        git add -a

Reconhece as mudanças de todos os arquivos existentes dentro do repositório

## Git rm

Remove arquivos que estão no index. Fazendo eles não serem rastreados pelo git. Completo oposto do add

        git rm readme.md

## Git commit

Adiciona as mudanças reconhecidas pelo git add e salva elas em uma versão única do repositório

        git commit -m "salvando as mudanças do git add ."

## Git Checkout
Realiza a verificação do repositório com o ambiente local. Verifica se está ou não atualizado. Ou também é utilizado para mudar de branches ou de tags. E também realiza a sincronia de versões de arquvios com o repositório

        git checkout [nome da branch] // Verifica se está atualizado e ou muda para uma branch
        git checkout -b nome_da_branch //criar a branche e muda o local da branch
        git checkout nome_do_arquivo // Força o arquivo local a ter as alterações do ultimo commit

## Git Reset --hard

Retorna forçosamente todos os arquivos para o a versão do último commit (HEAD)

## Git Clean
Remove arquivos e modificações que não foram rastreados pelo git. Ou seja, arquivos criados antes de sequer ter feito o git add --all

        git clean -f // remove tudo que não é rastreado pelo git de maneira forçada

## Git diff

verifica as alterações em detalhes de todos os arquivos

## .gitignore

arquivo que cria uma lista de arquivos que o git irá ignorar

## Git Log

Lista todas os commits realizados e também seus códigos de versionamento. Mostra também as tags associadas aos commits

## Git Branch
Lista todas as branches

        git branch nome_da_branch // cria uma branch com o nome especificado
        git branch -d/D nome_dabranch // deleta branche de nome especificado, se usar -D realiza de forma forçada

        git branch -m [nome_antigo] novo_nome // renomeia a branch atual para o novo_nome ou pode usar nome antigo caso não esteja na branch normal



## Git Push

Envia o último commit para o repositório local

        git push origin main //envia para a branch principal
        git push -u origin nome_da_branch // envia para a branch especificada no repositório

## Git Pull

Recebe do repositório a versão especificada pelo checkout e realiza o merge

Fetch + merge = pull

## Git Fetch

Baixa a última versão, mas não realiza o merge dos arquivos alterados

## Git Merge

Compara os arquivos de branches diferentes, ou do repositório remoto e local e faz a fusão de alterações, se esta não está na mesma linha. Caso haja alterações dos 2 arquivos na mesma linha, será necessário resolver os conflitos.

        git checkout main
        git merge develop // pega as alterações da branch develop e adiciona no branch main


## Git Tag

Cria tags em commits específicos

        git tag         // lista as tags
        git tag nome    //
        git tag -d/D nome : deleta a tag local
        git push -u origin nome_da_tag: adiciona a tag no repositório (aparece em releases)
        git push --delete origin nome: deleta a tag no repositório

## Git Stash

Adiciona modificações na pilha de memória

        git stash // add na pilha
        git stash list // mostra a lista de stashes na pilha
        git stash pop [nome] // puxa da pilha o stash mais recente. A não ser que você digite um nome de stash especifico

        git stash drop [nome] // remove da pilha o mais recente ou o stash nomeado

        git stash apply // aplica as modificações que estão em stash

## Git rebase

Deixas os commits em branches que serão mergeadas de forma linear para que não se criem commits adicionais na hora do merge. Isso se aplica quando há commits feitos em ambos as branches antes de ocorrer algum merge

Passo1: checkout na branch secundária -> git rebase primária

Passo2: checkout na branch primária -> git rebase secundária

## Alias

Cria atalhos nos códigos do git

Ex:
        git config --global alias.ch checkout //cria o atalho ch para o comando checkout

        git config --global --unset alias.ch // exclui o atalho criado

## Git Remote
Mostra a url daquele repositório específico

        git remove -v

## Grep
aplica filtros para listagens de branches, tags, commits e logs

ex:

    git branch | grep R1 // busca todas as branches que contenha R1








