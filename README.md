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

## Git Push

Envia o último commit para o repositório local

        git push origin main //envia para a branch principal

## Git Pull

Recebe do repositório a versão especificada pelo checkout e realiza o merge

Fetch + merge = pull

## Git Fetch

Baixa a última versão, mas não realiza o merge dos arquivos alterados

## Git Merge

Compara os arquivos de branches diferentes, ou do repositório remoto e local e faz a fusão de alterações, se esta não está na mesma linha. Caso haja alterações dos 2 arquivos na mesma linha, será necessário resolver os conflitos.

        git checkout main
        git merge develop // pega as alterações da branch develop e adiciona no branch main








