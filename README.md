# Comandos Git
Repositório com os comandos do git

Criar um novo repositório `git init`

Incluindo configuração de usuário `git config --global user.name Ricardo Silva`

Incluindo configuração de e-mail `git config --global user.email ricardocavalcantesilva@gmail.com`

Verificando a lista de alterações `git status`

Adicionar arquivos `git add <arquivo>` ou `git add *` onde * são todos os arquivos

Realizar commit `git commit -m "comentários das alterações"`

Verificando log `git log`

Criar Branch `git checkout -b NOME_BRANCH origin/master`

Excluir Branch Local `git branch -D NOME_BRANCH`

Verificando log em uma única linha `git log --oneline`

Clonando um repositório no github.com para o diretório físico `git@github.com:cavalsilva/ComandosGit.git`, exemplo clonando este repositório

Atualizar o repositório local com a nova versão do servidor remoto `git pull origin master`

Enviar as alterações do servidor local para o remoto `git push origin master`

Reverter mudanças `git reset --hard`

Remover todos arquivos e diretórios untracked `git clean -fd`, f (force) d (directory)

Atualizar configuração para nomes longos `git config core.longpaths true`

Descobrir última tag de um commit `git describe --contains <commit>`

# Git stash
O comando git stash salva as alterações sem commit (tanto as preparadas quanto as não preparadas). 

Por exemplo: Estou trabalhando direto na linha master e preciso criar uma branch para ela: `git stash`, depois faz a criação de uma nova branch `git checkout -b NOME_BRANCH` e por fim `git stash pop` (este comando pega o que foi gravado e coloca na branch), a partir daí é dar andamento na branch


# Rebase
Rebase
Antes da realização do rebase, verificar se tem algo na branch para ser commitada:

1 - `git status`

2 - caso tenha algo para commitar, realizar os commits e push

Realizando rebase com a master:

1 - `checkout master`

2 - `git pull`

Em seguida deve voltar para a branch para realizar o rebase interativo

1 - `git checkout NOME_BRANCH`

2 - `git rebase -i master`

Caso tenha algum conflito, deve ser feito os merges e em seguida confirmar as alterações do rebase:

1 - `git add .` (após o merge) 

2 - `git rebase --continue`

Por fim quando todo o rebase for concluído deve subir as alterações:

1 - `git push --force`
