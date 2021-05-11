###### Amend

Adicionar ao mesmo commit outras alteraçes (alterando também a mensagem do commit):
```
git commit --amend -m 'Correction in id type'
```
Necessário forçar o envio:
```
git push -f
```

Adicionar ao mesmo commit outras alteraçes (não alterando a mensagem do commit):
```
git commit --amend --no-edit
```
Necessário forçar o envio:
```
git push -f
```