# Stash

## O que é? / What is it?
**PT-BR**  
O comando git stash permite que você salve as alterações que você fez no seu diretório de trabalho, mas ainda não está pronto para fazer commit. Isso permite que você mude de branch ou atualize seu repositório sem perder suas alterações.

Muito importante ressaltar que o comando padrão, `git stash`, apenas salva as alterações de arquivos rastreados, sejam eles modificados ou na área de stage.

Uma opção é usar o comando `git add` e usar `git stash --staged` para salvar as alterações de arquivos que estão na área de stage ao stash.

***

**EN-US**  
The git stash command allows you to save the changes you made to your working directory, but are not yet ready to commit. This allows you to switch branches or update your repository without losing your changes.

It is very important to note that the default command, `git stash`, only saves changes to tracked files, whether they are modified or in the stage area.

An option is to use the `git add` command and use `git stash --staged` to save changes to files that are in the stage area to the stash.

***

## Comandos / Commands 
```bash

# Salva as alterações no stash
# Save changes to stash
git stash

# Salva as alterações na área de stage no stash
# Save changes in the stage area to stash
git stash --staged

# Lista os stashes
# List stashes
git stash list

# Aplica o primeiro stash da lista (index 0)
# Apply the first stash in the list (index 0)
git stash apply

# Aplica o stash de index n
# Apply the stash of index n
git stash apply stash@{n}

# Aplica o primeiro stash e remove ele da lista
# Apply the first stash and remove it from the list
git stash pop

# Aplica o stash de index n e remove ele da lista
# Apply the stash of index n and remove it from the list
git stash pop stash@{n}

# Remove o primeiro stash da lista
# Remove the first stash from the list
git stash drop

# Remove o stash de index n
# Remove the stash of index n
git stash drop stash@{n}

# Deleta todos os stashes
# Delete all stashes
git stash clear

# Cria um stash com um nome/mensagem
# Create a stash with a name/message
git stash save "name"
```