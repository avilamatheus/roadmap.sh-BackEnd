# Alias
**PT-BR**  
Alias é um comando que serve para criar um atalho para um comando do git. É muito útil para criar atalhos para comandos que são muito grandes ou que são utilizados com muita frequência.

***

**EN-US**  
Alias is a command that serves to create a shortcut for a git command. It is very useful for creating shortcuts for commands that are very long or that are used very frequently.

***

```bash
# Cria um alias para o comando "log --oneline", que lista os commits de forma resumida. Neste caso, o alias é "l" 
# Creates an alias for the log command, which lists the commits in a summarized way. In this case, the alias is "l"
git config --global alias.l "log --oneline"


# Para desfazer um alias, basta usar o comando "git config --global --unset alias.<alias_name>"
# To undo an alias, just use the command "git config --global --unset a
git config --global --unset alias.l

```

# Grep
**PT-BR**  
O comando `grep` é utilizado para buscar por um padrão em um arquivo. No caso do git, ele é utilizado para buscar por um padrão em um commit, por exemplo.

***

**EN-US**  
The `grep` command is used to search for a pattern in a file. In the case of git, it is used to search for a pattern in a commit, for example.

***

```bash
# Aqui estamos buscando por um commit que tenha a mensagem "commit message"
# Here we are searching for a commit that has the message "commit message"
git log --one-line | grep "commit message"
```