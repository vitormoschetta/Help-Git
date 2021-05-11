### SSH

Chaves SSH são uma forma segura de identificar usuários conhecidos, substituindo o tradicional "usuário e senha". Sua vantagem está na quantidade de caracteres em relação à uma senha tradicional, fazendo com que ataques bruteforce sejam inviabilizados devido ao tempo absurdo necessário para se "encontrar" a chave secreta através de tentativa e erro.

Esta chave pode ser gerada tanto no Windows quanto no Linux, e são um "par", sendo a chave pública (enviada para os servidores que você possui permissão para acessar) e a chave privada (somente você deve possuir e pode ser criptografada com uma senha).

Você pode adicionar a sua chave pública a mais de um usuário ou até mesmo em servidores diferentes, desde que você utilize sua chave privada para entrar nestes servidores (a qual por padrão fica salva em seu usuário no Linux), não terá nenhum problema.

<br>

#### GERAR CHAVE SSH LOCAL:

```
ssh-keygen -t <cryptography_type> -b <bit_lenght> -C "<user_email>"
```
exemplo:
```
ssh-keygen -t rsa -b 4096 -C "fulano@email.com"
```

#### Ir para o diretorio da chave

```
cd ~/.ssh/	
```

##### Lista as chaves SSH existentes 

```
ls	
```

##### Imprime a chave SSH publica na tela

```
cat id_rsa.pub
```

Agora é só copiar a chave gerada e colar no local indicado no seu repositório remoto.
		

#### Vincular repositório local ao GitHub:  
```
git remote add origin git@github.com:<username>/repositorio.git
```



<br>
<br>

##### Referências

<https://tecdicas.com/como-criar-e-utilizar-chaves-ssh-no-windows-e-linux>

<https://adrianorosa.com/blog/seguranca/ssh-keys.html>