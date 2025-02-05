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



