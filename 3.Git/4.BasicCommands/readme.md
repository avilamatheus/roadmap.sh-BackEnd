# Comandos Básicos / Basic Commands

## Configuração do Usuário / User Configuration
```bash

git config --global user.name "My Name"
git config --global user.email "myemail@gmail.com"


# Verificando a configuração / Verifying the configuration

git config --global user.name
git config --global user.email
git config --list    
```

## Criando um repositório local / Creating a local repository
```bash
git init
```

## Verificando o status do repositório / Checking the repository status
```bash
git status
```

## Adicionando arquivos à área de stage / Add files to the staging area
```bash
#Adiciona um arquivo específico / Adds a specific file
git add file.txt

#Adiciona todos os arquivos / Adds all files
git add .
git add -A
git add --all
```

## Fazendo o git parar de rastrear um arquivo / Making git stop tracking a file
```bash
git rm --cached file.txt
```

## Commitando arquivos / Committing files
```bash
git commit -m "Commit message"
```

## Visualizando alterações / Viewing changes
```bash
# Visualiza diferenças entre o workspace e a área de stage
git diff

# Visualiza diferenças entre a área de stage e o último commit
git diff --staged

# Visualiza diferenças entre o workspace e o último commit
git diff HEAD
```

## Histórico de commits / Commit history
```bash
git log
```

Exemplo de saída / Output example:
```bash
commit c55971099240ec7af47fcad47bb6993fd7272a43 (HEAD -> master, origin/master, origin/HEAD)
Author: Matheus Avila <matheus.avila@grad.ufsc.br>
Date:   Mon Feb 19 18:40:32 2024 -0300

    Four States readme

#c55971099240ec7af47fcad47bb6993fd7272a43 é o hash do commit / is the commit hash

#HEAD é o ponteiro para o último commit / is the pointer to the last commit

#master é o nome do branch / is the branch name

#origin/master e origin/HEAD são ponteiros para o último commit no repositório remoto / are pointers to the last commit in the remote repository

#Author é o autor do commit e seu email / is the commit author and his email

#Date é a data e hora do commit / is the commit date and time

#Four States readme é a mensagem do commit / is the commit message

```
Para sair do log, pressione a tecla "q" / To exit the log, press the "q" key.

### Variações do log / Log variations
```bash
# Log com um commit por linha / Log with one commit per line
git log --oneline

# Log mostrando N commits / Log showing N commits
git log -N

# Log mostrando N commits com um commit por linha / Log showing N commits with one commit per line
git log -N --oneline

# Log mostrando as diferenças entre os commits / Log showing the differences between commits
git log -p

# Mostra os arquivos alterados em cada commit / Shows the files changed in each commit
git log --stat

# Versão resumida do stat / Short version of stat
git log --shortstat
```

## Alterando o último commit / Changing the last commit
```bash
git commit --amend -m "New commit message"

# ou caso não queira alterar a mensagem do commit anterior / or if you don't want to change the previous commit message
git commit --amend --no-edit
```

## Navegando entre commits / Navigating between commits
```bash
git checkout <hash>

# Para voltar ao HEAD / To return to HEAD
git checkout master
```

## Desfazendo alterações / Undoing changes
**PT-BR**  
Se um arquivo não estiver na staging area (ou seja, não foi adicionado com git add), mas foi modificado no diretório de trabalho, o comando `git checkout` desfaz as alterações desse arquivo (desde que o mesmo esteja rastreado).

Se um arquivo estiver na staging area e foi modificado no diretório de trabalho, o comando `git checkout` desfaz as alterações desse arquivo no diretório de trabalho e substitui pela versão que está na staging area, restaurando-o para o estado em que estava quando foi adicionado à staging area.

**EN-US**  
If a file is not in the staging area (i.e. it was not added with git add), but was modified in the working directory, the `git checkout` command undoes the changes to that file (as long as it is tracked).

If a file is in the staging area and was modified in the working directory, the `git checkout` command undoes the changes to that file in the working directory and replaces it with the version that is in the staging area, restoring it to the state it was in when it was added to the staging area.
***

```bash
# Desfaz as alterações em um arquivo especifico.
# Undoes changes in a specific file
git checkout file.txt

# Desfaz alterações em tudo.
# Undoes changes in everything
git checkout .

# Remove arquivos não rastreados
# Removes untracked files
git clean -f

# Desfaz alterações em tudo, 
# inclusive em arquivos na área de stage,
# menos novos 
# arquivos em stage.
# Porém, para funcionar, é necessário que o repo tenha ao menos um commit.

# Undoes changes in everything,
# including files in the staging area,
# except new files in the staging area.
# However, to work, the repo must have at least one commit.
git checkout HEAD .
```

## Removendo arquivos da área de stage / Removing files from the staging area
```bash
# Remove um arquivo específico / Removes a specific file
git reset <file>

# Remove tudo da área de stage / Removes everything from the staging area
git reset

# Remove tudo da area de stage e descarta todas as alterações rastreadas, incluindo novos arquivos em stage.
# Removes everything from the staging area and discards all tracked changes, including new files in the staging area.
git reset --hard
```

***
![Desfazendo mudanças](image.png)
***

## Gitignore
Ignora arquivos e diretórios / Ignores files and directories.

Exemplo:
```bash
# Arquivos .txt
*.txt

# Diretório / Directory
diretorio/
```

### Uma coleção de templates .gitignore: / A collection of .gitignore templates
https://github.com/github/gitignore

## Parar de rastrear um arquivo / Stop tracking a file
```bash

#Assumindo que o arquivo foi colocado no .gitignore / Assuming the file was put in .gitignore

git update-index --skip-worktree file.txt

# Para voltar a rastrear / To start tracking again
git update-index --no-skip-worktree file.txt
```

## Clonando um repo / Cloning a repo
```bash
# clonando localmente / cloning locally
git clone /path/to/repo /path/to/newrepo

# clonando de um repositório remoto / cloning from a remote repository
git clone git@github.com:DevMasterTeam/Udemy-Git.git
