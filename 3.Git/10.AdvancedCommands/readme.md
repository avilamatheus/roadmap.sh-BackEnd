# Comandos Avançados / Advanced Commands

## Commit com add / Commit with add
```bash
git commit -a -m "commit msg"

# É importante ressaltar que o comando acima adiciona todos os arquivos modificados no commit, porém não adiciona arquivos novos que não foram adicionados no stage, aka arquivos untracked.
# It is important to note that the above command adds all modified files to the commit, but does not add new files that have not been added to the stage, aka untracked files.
```

## Revertendo um Commit / Reverting a Commit
```bash
git revert <commit> 
#or
git revert HEAD
#or
git revert <commit> --no-edit
```

## Desfazendo um Commit / Undoing a Commit
```bash

# Desfaz commits e descarta as alterações feitas no código
# Undoes commits and discards changes made in the code
git reset --hard HEAD~n
# n = número de commits que deseja desfazer
# n = number of commits to undo

# Desfaz commits mas mantém as alterações feitas no código, porém remove da area de stage
# Undoes commits but keeps the changes made in the code, but removes from the stage
git reset --mixed HEAD~n
# n = número de commits que deseja desfazer
# n = number of commits to undo

# Desfaz commits mas mantém as alterações feitas no código, e mantém na area de stage
# Undoes commits but keeps the changes made in the code, and keeps in the stage
git reset --soft HEAD~n
# n = número de commits que deseja desfazer
# n = number of commits to undo
```
***
**PT-BR**  
Caso queira recuperar o commit desfeito, utilize o comando abaixo, (Considerando que o commit desfeito foi salvo no repositório remoto):

**EN-US**  
If you want to recover the undone commit, use the command below, (Assuming the undone commit was saved in the remote repository):
***
```bash
git pull
```

## Forçar um Push / Force a Push
```bash
# Sobrecreve o repositório remoto com o repositório local, independente de qualquer coisa, podendo fazer com que commits de outros usuários sejam perdidos
# Overwrites the remote repository with the local repository, regardless of anything, which may cause other users' commits to be lost
git push --force

# Sobrecreve o repositório remoto com o repositório local, porém verifica se houve alterações no repositório remoto antes de fazer o push, evitando que commits de outros usuários sejam perdidos
# Overwrites the remote repository with the local repository, but checks if there were changes in the remote repository before pushing, avoiding other users' commits from being lost
git push --force-with-lease
```
***

**PT-BR**  
É importante ressaltar que o comando `git push --force` é muito perigoso e deve ser usado em situações específicas e com muita cautela, portanto deve ser evitado ao máximo. 
***

**EN-US**  
It is important to note that the `git push --force` command is very dangerous and should be used in specific situations and with great caution, so it should be avoided as much as possible.

## Rebase
**PT-BR**  
Basicamente o Rebase serve para evitar um merge commit, a fim de não poluir o histórico de commits, mantendo-o mais limpo e organizado. O Rebase é muito útil quando se trabalha com branches, pois evita que o histórico de commits fique poluído com muitos merge commits.
***

**EN-US**  
Basically Rebase serves to avoid a merge commit, in order not to pollute the commit history, keeping it cleaner and more organized. Rebase is very useful when working with branches, as it prevents the commit history from being polluted with many merge commits.
***

```bash
# Rebase de um branch em outro
# Rebase from one branch to another
git rebase <branch>

# Abortando rebase caso ocorra algum conflito
# Aborting rebase if there is a conflict
git rebase --abort

# Continuando rebase caso ocorra algum conflito e o mesmo seja resolvido
# Continuing rebase if there is a conflict and it is resolved
git rebase --continue

# Git pull com rebase, evitando um merge commit automatico ao fazer um pull
# Git pull with rebase, avoiding an automatic merge commit when doing a pull
git pull --rebase
```

## Rebase Squash
**PT-BR**  
Serve para juntar vários commits em um único commit, mantendo o histórico de commits mais limpo e organizado. Para tal, precisamos utilizar o comando `git rebase -i HEAD~n`, onde `n` é o número de commits que queremos juntar.

***

**EN-US**  
It serves to join several commits into a single commit, keeping the commit history cleaner and more organized. To do this, we need to use the `git rebase -i HEAD~n` command, where `n` is the number of commits we want to join.
***
```bash
# Rebase Squash
git rebase -i HEAD~n
# n = número de commits que queremos juntar
# n = number of commits we want to join
```
***
**PT-BR**  
No editor que abrir, troque a palavra `pick` por `squash` nos commits que deseja juntar, e salve o arquivo. Em seguida, será aberto um novo editor para que você possa escrever a mensagem do novo commit que será criado.

**EN-US**  
In the editor that opens, change the word `pick` to `squash` in the commits you want to join, and save the file. Then a new editor will open so you can write the message of the new commit that will be created.



## Recriando branch a partir do repositório remoto / Recreating branch from remote repository
```bash
# Deleta a branch local
# Deletes the local branch
git branch -d <branch>
#or
git branch -D <branch>

# Puxa a branch do repositório remoto
# Pulls the branch from the remote repository
git fetch origin <branch>

# Troca para a branch
# Switches to the branch
git checkout <branch>
```

## Cherry Pick
**PT-BR**  
Cherry Pick é um comando que serve para pegar um commit de uma branch e aplicar em outra branch. É muito útil quando se quer pegar um commit específico de uma branch e aplicar em outra branch, sem precisar aplicar todos os commits da branch.

***

**EN-US**  
Cherry Pick is a command that serves to take a commit from one branch and apply it to another branch. It is very useful when you want to take a specific commit from one branch and apply it to another branch, without having to apply all the commits from the branch.

***
```bash
# Pega um commit de uma branch e aplica na branch atual
# Takes a commit from one branch and applies it to the current branch
git cherry-pick <commit>
```

## Bisect
**PT-BR**  
O comando `git bisect` serve para encontrar um commit que introduziu um bug em um projeto. O comando faz uma busca binária entre os commits, onde o usuário informa um commit que possui o bug e um commit que não possui o bug, e o comando faz a busca binária entre esses dois commits.

***

**EN-US**  
The `git bisect` command serves to find a commit that introduced a bug in a project. The command performs a binary search between the commits, where the user informs a commit that has the bug and a commit that does not have the bug, and the command performs the binary search between these two commits.

***

```bash
# Inicia o bisect
# Starts the bisect
git bisect start

# Informa um commit que não possui o bug
# Informs a commit that does not have the bug
git bisect good <commit>

# Informa um commit que contém o bug
# Informs a commit that contains the bug
git bisect bad <commit>

# Após informar os commits, o comando fará a busca binária entre os commits informados. 
# Esse processo irá continuar até que o commit que introduziu o bug seja encontrado, exigindo que o usuário informe o commit good e/ou bad a cada iteração.

# After informing the commits, the command will perform the binary search between the informed commits.
# This process will continue until the commit that introduced the bug is found, requiring the user to inform the good and/or bad commit at each iteration.

# Após encontrar o commit que introduziu o bug, o comando irá informar o commit que introduziu o bug.
# After finding the commit that introduced the bug, the command will inform the commit that introduced the bug.

# Finaliza o bisect
# Ends the bisect
git bisect reset
```

## Fetch
**PT-BR**  
O comando `git fetch` serve para baixar as alterações do repositório remoto, porém não aplica as alterações no repositório local, apenas baixa as alterações para que o usuário possa visualizar as alterações que foram feitas no repositório remoto. Ou seja, é basicamente um `git pull` sem aplicar as alterações no repositório local.

***

**EN-US**  
The `git fetch` command serves to download changes from the remote repository, but does not apply the changes to the local repository, only downloads the changes so that the user can view the changes that were made in the remote repository. That is, it is basically a `git pull` without applying the changes to the local repository.

***

```bash
# Baixa as alterações do repositório remoto
# Downloads changes from the remote repository
git fetch

# Para visualizar todas as branches, inclusive as do repositório remoto
# To view all branches, including those from the remote repository
git branch --all

# Para visualizar as alterações que foram baixadas
# To view the changes that were downloaded
git log origin/<branch>

# Troca para a branch que deseja aplicar as alterações
# Switches to the branch to apply the changes
git checkout <branch>

# Aplica as alterações no repositório local
# Applies the changes to the local repository
git merge origin/<branch>
```