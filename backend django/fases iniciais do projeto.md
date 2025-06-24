![[Pasted image 20250204224424.png]]
utilizamos esse comando para verificar qual o banco de dados que foi informado no `settings.py`  que será utilizado, por padrão o django já vem com o sqlite3 mas é possível alterar. Ao rodar este comando, o django criará um banco de dados para este projeto.
Se tudo der certo, a seguinte tela aparecerá:
![[Pasted image 20250204225322.png]]

Após isso, para iniciarmos o servidor, usamos o seguinte comando:
![[Pasted image 20250204225723.png]]
e assim, nosso servidor terá sido inicializado e poderemos clicar para abrir o mesmo em nosso navegador.


## Administração e configuração do banco de dados

Para podermos administrar o banco de dados dentro da nossa aplicação django, precisamos criar quase como um novo app, utilizando do comando:

![[Pasted image 20250204231631.png]]
- Sendo "administracao" nesse caso o nome do novo "app"
- O arquivo de models será onde vamos escrever instruções para o banco de dados

Para cada app criado é preciso também colocar o nome dele no arquivo de settings, para isso, basta procurar a aba de `instaled_apps` e colocar o nome do aplicativo.
![[Pasted image 20250204232322.png]]

## Acesso ao painel administrativo do django
Para acessarmos precisamos na url do nosso site, colocarmos `/admin`, dessa forma:
![[Pasted image 20250205132227.png]]
Assim, acessamos o painel administrativo do nosso projeto em django.

Para acessarmos de fato, vamos precisar de um usuário e uma senha, para isso, executamos o código:
![[Pasted image 20250205132503.png]]
e escrevemos o nome de usuário, o email se quiser e a senha.

## Como jogar a tabela do banco de dados para o painel administrativo
Podemos jogar a tabela que foi criada anteriormente em nosso arquivo models para o painel administrativo do django, para isso precisamos do arquivo "admin.py", dentro dele vamos importar a tabela para ele:
![[Pasted image 20250205192812.png]]
- Topic nesse caso é o nome da tabela que iremos passar para o painel administrativo.

Agora para registrar a tabela no painel temos o seguinte código:
![[Pasted image 20250205193043.png]]
- Aqui estamos usando uma função que vai registrar a nossa tabela no painel e estamos passando que queremos que registre "Topic" que nesse caso, é nossa tabela.

E deverá ficar assim:
![[Pasted image 20250205193229.png]]
Com a tabela criada registrada no painel.



