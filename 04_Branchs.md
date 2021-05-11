## Trabalhando com Branchs

#### CONSULTANDO AS BRANCHS EXISTENTES:
```
git branch
```

Obs: ELE VAI DESTACAR A BRANCH ATUAL COM UM * (ASTERISCO)

#### CRIAR UMA BRANCH:
```
git checkout -b <branch_name>
```

#### ALTERAR O NOME DA BRANCH ATUAL
```
git branch -m <branch_name>
```

#### MUDAR DE BRANCH:
```
git checkout <branch_name>
```

#### DELETANDO A BRANCH 'TESTE'
```
git branch -D <branch_name>
```

#### MESCLANDO ALTERAÇÕES FEITAS EM OUTRA BRANCH:
Necessário estar na branch em que se deseja receber as atualizações:
```
git merge <branch_name>
```

O nome da branch no comando acima deve ser a origem da atualização, ou seja, a branch do qual se deseja trazer o código fonte.


#### MESCLAGEM DIRETA:
```
git merge <destino> <origem>
```