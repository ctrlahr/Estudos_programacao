O models é uma ferramenta do django que vai permitir com que você crie tabelas, modifique-as, etc. Ele vai permitir você administrar o banco de dados sem escrever código SQL. 

Esse processo é feito por meio da criação de classes
![[Pasted image 20250204233959.png]]

Este código faz o seguinte...
- Primeiro é criada uma classe cujo nome dado foi "Topic", depois fazemos ela herdar de `models.model` que é a classe base do django para modelos de banco de dados, fazendo da classe "topic", uma tabela no banco de dados.
- Logo depois criamos uma variável que será um item na tabela do banco de dados e falamos que ela será um texto por meio do `CharField` e limitamos seu tamanho para 200.
- Criamos outra variável, entretanto, essa armazena tanto data quanto hora, por meio do `DateTimeField`. Logo depois fazemos com que a data seja automaticamente preenchida quando um novo tópico for criado, ou seja, quando um novo tópico for adicionado automaticamente esse campo será preenchido, isso graças ao `auto_now_add = True`.
- Depois criamos um método especial do python que é o método `str` que determina como o objeto será representado como string e ele é chamado automaticamente ao tentarmos converter um objeto para texto
- Logo abaixo, em `return self.text` estamos falando que quando o objeto topic precisar ser exibido como um texto ele retornará o conteúdo do campo text, que anteriormente foi criado

Para passarmos isso para o banco de dados nós precisamos digitar o seguinte comando:
![[Pasted image 20250204235320.png]]
- Sendo `estudo_django/manage.py` o diretório do seu arquivo `manage.py`

E depois disso, rodamos o seguinte código para subir a(s) tabela(s) para o banco de dados:
![[Pasted image 20250204235552.png]]
- Sendo novamente `estudo_django/manage.py` o diretório do seu arquivo `manage.py`

Logo após fazer esses passos se você olhar no seu banco de dados verá que a tabela estará lá, com o que foi dado a classe que representava ela.
![[Pasted image 20250204235832.png]]