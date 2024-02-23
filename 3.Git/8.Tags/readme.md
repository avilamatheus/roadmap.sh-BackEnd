# Tags

## O que é? / What is it?
**PT-BR**  
Tags são utilizadas para marcar versões de um projeto e estão associadas a um commit específico, podendo ser utilizadas para marcar releases, versões de correções, versões de novas funcionalidades, etc. Em resumo, tags são um ponteiro para um commit específico.

***

**EN-US**  
Tags are used to mark versions of a project and are associated with a specific commit, and can be used to mark releases, versions of fixes, versions of new features, etc. In short, tags are a pointer to a specific commit.

***

## Tipos de tag / Tag types

### Lightweight
**PT-BR**  
São tags simples, que apontam para um commit específico, sem informações adicionais.

**EN-US**  
Are simple tags, that point to a specific commit, without additional information.

Exemplo / Example:
```bash
# Criando uma tag lightweight no commit atual
# Creating a lightweight tag in the current commit
git tag <tag_name>

# Criando uma tag lightweight em um commit específico
# Creating a lightweight tag in a specific commit
git tag <tag_name> commit_hash
```

### Annotated
**PT-BR**  
É uma tag que contém informações adicionais, como o nome do autor e uma mensagem.

**EN-US**  
It is a tag that contains additional information, such as the author's name and a message.

Exemplo / Example:
```bash
# Criando uma tag annotated no commit atual
# Creating an annotated tag in the current commit
git tag -a -m "Release v1.0.0" <tag_name>

# Criando uma tag annotated em um commit específico
# Creating an annotated tag in a specific commit
git tag -a -m "Release v1.0.0" <tag_name> commit_hash
```

## Listando tags / Listing tags
```bash
# Listando todas as tags
# Listing all tags
git tag

# Listando todas as tags e sua mensagem
# Listing all tags and their message
git tag -n

# Listando todas as tags e o commit associado
# Listing all tags and the associated commit
git show-ref --tags
```

## Enviando tags para o repositório remoto / Sending tags to the remote repository
```bash
# Enviando uma tag específica para o repositório remoto
# Sending a specific tag to the remote repository
git push origin <tag_name>

# Enviando todas as tags para o repositório remoto
# Sending all tags to the remote repository
git push origin --tags
```

## Usando tags como referência / Using tags as reference
```bash
# Navegar para um commit específico usando a tag
# Navigate to a specific commit using the tag
git checkout <tag_name>

# Comparar diferenças entre tags
# Compare differences between tags
git diff <tag_name1> <tag_name2>
```

## Removendo tags / Removing tags

### Localmente / Locally
```bash
git tag -d <tag_name>
```

### No repositório remoto / In the remote repository
```bash
git push --delete origin <tag_name>
```