#### GIT STASH

##### Guardar alterações feitas e ainda não comitadas em uma branch temporária:
```
git stash
```
Obs: o comando acima guarda apenas arquivos já rastreados.  
Para novos arquivos adicionados usar o seguinte comando:
```
git stash push -m <name> --include-untracked 
```
ou abreviado:
```
git stash push -m <name> -u
```

##### Guardar alterações feitas em um arquivo específico:
```
git stash push -m readme README.md
```
Veja que ainda podemos dar um nome (-m readme) ao stash


##### Visualizar lista de stash existentes:
```
git stash list
```
A saída é parecido com isto:
```
stash@{0}: WIP on feature/Add-unit-tests-for-ProductCategory...
stash@{1}: WIP on feature/add-unit-tests-for-clientsettings...
```


##### Listar arquivos em stash:
```
git stash show
```


##### Visualizar diff de uma stash específica:
```
git stash show -p stash@{0}
```



##### Aplicar um stash específico
```
git stash apply stash@{0}
```


##### Aplicar todos os stashs salvo na branch atual
```
git stash pop
```
ou 
```
git stash apply
```


##### Dropar um stash especifico
```
 git stash drop stash@{0}
```


##### Dropar ultimo stashs
```
 git stash drop
```
