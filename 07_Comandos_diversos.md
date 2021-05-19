
#### LOG DO USUARIO ATUAL:
```
git log
```
#### LOG DE TODOS OS USUARIOS:
```
git shortlog
```
#### LOG COM GRAFICOS:
```
git log --graph
```
#### MOSTRA DETALHES DE UM COMMIT (DETALHE DAS MODIFICAÇÕES):
```
git show + 'hash'  
```
Obs: 'hash' é a sequencia de caracteres que identifica o commit

#### OLHAR AS MUDANÇAS FEITAS NO CODIGO FONTE DOS ARQUIVOS ANTES DE COMITAR:
```
git diff 
```
#### OLHAR OS ARQUIVOS MODIFICADOS (APENAS O NOME DOS ARQUIVOS):
```
git diff --name-only
```
#### CANCELAR ARQUIVO MOTIFICADO ANTES DE LER (GIT ADD):
Desfazer modificações de um arquivo apenas:
```
git checkout Leiame.txt
```

Desfazer todas as modificações (arquivos  já rastreados):
```
git checkout -- .
```

Remover todos os arquivos adicionados (novos arquivos / não rastreados):
```
git clean -f -d
```

####  CANCELAR ARQUIVO MODIFICADO DEPOIS DE JÁ TER FEITO 'git add'
```
git reset HEAD Leiame.txt   
```
Obs: ESSE COMANDO RETIRA O ARQUIVO DO 'STAGED', POSSIBILITANDO EXECUTAR O COMANDO 'git checkout ..'

#### CANCELAR O ARQUIVO DEPOIS DE TER FEITO COMMIT:
```
git reset  (palavra chave) + 'hash' 
```

Obs: PALAVRAS CHAVES SÃO 3, CONFORME ABAIXO:
```
--soft
```
VOLTA PARA STAGED, PRONTO PARA COMITAR NOVAMENTE
```
--mixed
```
VOLTA PARA UNTRACKED,  PARA SER LIDO NOVAMENTE
```
--hard
```
DELETA A MUDANÇA / APAGA, SOME..


## VERSINAMENTO COM TAGS 

Para criar versões da sua aplicação.

```
git tag -a 1.0.0 -m "Estrutura Inicial Projeto Core MVC"

git push origin master --tags
```


#### APAGAR TAG:
```
git tag -d 1.0.0 	
git push origin :1.0.0 
```


#### DEFINIR ARQUIVO PARA TEXTO DE COMMITS:
```
git config --global commit.template ~/.gitmessage.txt
```


<br>
