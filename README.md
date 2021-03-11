## Git

#### CONFIGURAÇÃO LOCAL

```
git init

git config --global user.name "user name"
git config --global user.email "email"
```

#### SSH

###### GERAR CHAVE SSH LOCAL:

```
ssh-keygen -t rsa -b 4096 -C "email"
```

###### Ir para o diretorio da chave

```
cd ~/.ssh/	
```

###### Lista as chaves SSH existentes 

```
ls	
```

###### Imprime a chave SSH publica na tela

```
cat id_rsa.pub
```

Agora é só copiar a chave gerada e colar no local indicado no seu repositório remoto.
		
    

#### ADICIONAR REPOSITORIO 
```
git remote add origin git@github.com:username/repositorio.git
```


#### CRIANDO E/OU ENTRANDO EM DIRETORIOS/PASTAS
```
mkdir nomeDaPasta

cd nomeDaPasta/
```

#### VERIFICAR SE HÁ ARQUIVOS PARA ADD OU FAZER COMMIT:
```
git status
```

#### ADD UM NOVO ARQUIVO OU ALTERAÇÃO FEITA:

###### Adicionar arquivo específico:
```
git add Leiame.txt
```

###### Adicionar todos os arquivos:
```
git add .
```

#### FAZER COMMIT:
```
git commit -m "Comentario..."
```

#### FAZER PUSH (ENVIAR ALTERAÇÕES PARA O DIRETORIO REMOTO):
```
git push orign master 	=> master é a branch padrão, pode ser outra branch criada por vc
```

#### VERIFICA O DIRETORIO REMOTO CONFIGURADO:
```
git remote -v
```


## Trabalhando com Branchs

#### CONSULTANDO AS BRANCHS EXISTENTES:
```
git branch
```

Obs: ELE VAI DESTACAR A BRANCH ATUAL COM UM * (ASTERISCO)

#### CRIAR UMA BRANCH COM NOME 'TESTE'
```
git checkout -b teste
```

#### MUDAR DE BRANCH:
```
git checkout master => por o nome da branch que deseja usar
```

#### DELETANDO A BRANCH 'TESTE'
```
git branch -D teste
```

#### MESCLANDO ALTERAÇÕES FEITAS EM OUTRA BRANCH:
```
git merge teste
```
Obs : No exemplo acima estou trazendo as alterações feita na branch 'teste' para  a branch atual


## OUTROS COMANDOS UTEIS 

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



#### ATUALIZAR DIRETÓRIO COM ATUALIZAÇÕES MAIS RECENTES DA BRANCH:
```				
git pull
```
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
```
git checkout Leiame.txt
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
