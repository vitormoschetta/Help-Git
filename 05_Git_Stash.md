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


###### Visualizar lista de stash existentes:
```
git stash list
```
A saída é parecido com isto:
```
stash@{0}: WIP on feature/Add-unit-tests-for-ProductCategory...
stash@{1}: WIP on feature/add-unit-tests-for-clientsettings...
```


###### Visualizar diff de uma stash específica:
```
git stash show -p stash@{0}
```
