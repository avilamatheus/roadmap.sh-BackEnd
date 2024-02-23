# Merge

## Merge branch na master / Merge branch into master
```bash
git checkout master
git merge <branch_name>
```
***

## Listar branches que não sofreram merge / List branches not merged
```bash
git branch --no-merged
```

## Listar branches que sofreram merge / List branches merged
```bash
git branch --merged
```

## Abortar um merge / Abort a merge
```bash
git merge --abort
```

## Resolver conflitos / Resolve conflicts
```bash
git merge <branch_name>
```

**PT-BR**  
Considerando que haja um conflito e o mesmo seja resolvido, é necessário adicionar as alterações e realizar o commit.

**EN-US**  
Considering that there is a conflict and it is resolved, it is necessary to add the changes and commit.

```bash
git add .
git commit -m "merge conflict resolved"
```
***
