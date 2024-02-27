# Branches

## O que é uma branch? / What is a branch?
**PT-BR**  
Branch é uma ramificação do projeto. É uma cópia do projeto em um determinado momento, que pode ser alterada sem afetar o projeto principal.

É usado para desenvolver novas funcionalidades, corrigir bugs, testar novas ideias, etc, sem interferir no projeto principal (branch master ou main).

Quando uma branch é incluída no projeto principal, ela é mesclada (merge) com o projeto principal.

***

**EN-US**  
Branch is a project branch. It is a copy of the project at a certain moment, which can be changed without affecting the main project.

It is used to develop new features, fix bugs, test new ideas, etc, without interfering with the main project (master or main branch).

When a branch is included in the main project, it is merged with the main project.

***

## Comandos / Commands

### Listar branches / List branches
```bash
git branch
#or
git branch --list

# Lista todas as branchs, inclusive as do repositório remoto
# Lists all branches, including those from the remote repository
git branch -a 
#or
git branch --all
```

### Criar uma branch / Create a branch
```bash
git branch <branch_name>
```

### Mudar para uma branch / Switch to a branch
```bash
git checkout <branch_name>
#or
git switch <branch_name>
```

### Criar uma branch no repositório remoto / Create a branch in the remote repository
```bash
git push -u origin <branch_name>
```

### Removendo branchs locais / Removing local branches
```bash
git branch -d <branch_name>

# Força a remoção da branch, mesmo que haja commits não mesclados
# Forces the removal of the branch, even if there are unmerged commits
git branch -D <branch_name>

```

### Removendo branchs remotas / Removing remote branches
```bash
git push origin --delete <branch_name>
```

### Renomear branch local / Rename local branch
```bash
# Renomeia a branch atual / Rename the current branch
git branch -m <new_branch_name>

# Renomeia uma branch específica / Rename a specific branch
git branch -m <old_branch_name> <new_branch_name>
```

### Ver commits de uma branch específica / View commits from a specific branch
```bash
git log <branch_name>
#or
git log <branch_name> --oneline
```
