#### GIT STASH

###### Guardar alterações feitas e ainda não comitadas em uma branch temporária:
```
git stash
```
Obs: o comando acima guarda apenas arquivos já rastreados.  
Para novos arquivos adicionados usar o seguinte comando:
```
git stash --include-untracked 
```
ou abreviado:
```
git stash -u
```

###### Listar arquivos em stash:
```
git stash show
```

###### Listar alterações em stash:
```
git stash show -u
```

###### Aplicar stash salvo na branch atual
```
git stash pop
```
ou 
```
git stash apply
```