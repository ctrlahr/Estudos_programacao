## Spring web



## Spring Data JPA
Sua sigla significa "java persistence API", a spring data JPA é uma dependência que permite com que o dev trabalhe com banco de dados SQL no projeto spring.
É uma abstração(Maneira de simplificar um processo) que permite trabalhar com banco de dados. 
O JPA também oferece diversos métodos que permitem com que o processo de [[serialização de dados]] se torne muito mais fácil, permitindo a realização de queries por meio desses métodos oferecidos.


##### `findAll()`
O método `findAll` retorna todas as informações de uma tabela específica.


##### `findById()`
O `findById` é utilizado para acessar algo especificando o id, ele é utilizado em conjunto com o [[Optional]] 

##### `save()`
O método save faz uma [[serialização de dados||serialização de dados inversa]], onde é pegado um json enviado pelo usuário e esse json é passado para o banco de dados. 
O método save é bastante utilizado em operações de atualizar algo no Db por ter a função que se um id existente for passado o conteúdo será modificado.

##### `deleteById()`
Como o próprio nome já fala, deleta algo da tabela sendo específicado por id. No caso da utilização no spring é necessário a criação do método no `service` e de outro método no `controller`, assim como os outros.

*Service:*
![[Pasted image 20250712010918.png]]
- É criada uma função que não retorna nada e ela recebe um `Long` id como parâmetro
- Posteriormente apenas é utilizado da injeção de dependência para fazer uso do método `deleteById` e passar como parâmetro o id 


*controller:*
![[Pasted image 20250712010941.png]]
- No controller, é definido que o parâmetro da função para deletar é uma variável de caminho, sendo assim, é necessário passar o id do que deve ser removido do Db pela URL da aplicação.
- Depois, apenas é chamada a função criada no `service` por meio da injeção de dependência do mesmo
- Por fim apenas é retornado algo para o usuário ter ciência que algo foi deletado.


##### ORM
A dependência do JPA traz junto o ORM que uma de suas funcionalidades é atuar como um scanner que vai escanear a classe pedida e vai passar seus atributos para o banco de dados, basicamente traduzindo o código java em código que o banco de dados entenda.
Para utilizar dessa funcionalidade do ORM é necessário extender o `JpaRepository` em alguma interface ou classe como uma interface de repository que vai conectar o banco de dados ao código:
![[Pasted image 20250704133005.png]]
- é necessário passar a classe que o JPA quer que o ORM fique escaneando
- Também é necessário passar o tipo de dado do ID da classe.

É válido lembrar que quando se tenta deletar um item que está como chave estrangeira pra outra tabela não é possível deletar justamente por que o outro item da outra tabela necessita que o elemento da chave estrangeira exista.


O ORM funciona quase que como um tradutor da linguagem que está sendo utilizada para a linguagem do banco de dados. Ele vai mapear toda a classe passada para ele e vai traduzir para o DB.
![[Pasted image 20250704134700.png]]

##### Hibernate
Hibernate é um organizador, após a tradução que o ORM faz para o banco de dados o hibernate faz a organização, pegando o mapeamento da classe e transformando em forma de tabela.



## LomBok
O Lombok é utilizado para facilitar a criação de construtores, então, é possível criar construtores `AllArgs` e `NoArgs` de forma muito mais fácil, a anotação do lombok apenas precisa estar em cima da classe:
![[Pasted image 20250703110638.png]]

o lombok também cria getters e setters, basicamente da mesma forma, usando a anotação de `@data` em cima da classe:
![[Pasted image 20250703111003.png]]



## Bancos de dados
Para trabalhar com bancos de dados é necessário baixar a dependência relativa ao banco de dados e adicionar ao `pom.xml` no caso do maven, segue um exemplo com o H2: 
![[Pasted image 20250704143724.png]]



## Flyway
O flyway é a maneira do Java e do Spring de utilizar [[Migrations]], essas migrations devem ficar localizadas dentro da pasta migration e cada migration precisa de uma sintaxe específica para o flyway ser capaz de encontra-la.
Elas necessitam ter na frente um "V" maiúsculo com o número da migration, por exemplo: "V1" seguido de  dois underlines:
`V1__nome_da_migration.sql`

Mas para que tudo isso funcione é necessário realizar a conexão com o banco de dados, isso é feito no `aplication.properties`, dessa forma:
![[Pasted image 20251216225854.png]]
- É necessário colocar a `url` do banco de dados junto como nome de usuário e a senha


## Spring security
O Spring security é uma dependência que visa adicionar mais proteção as aplicações spring. Utilizando de métodos de autenticação, necessidade por padrão de credenciais para chamados de requisições, etc.

*Token CSRF*
[[CSRF |Token CSRF]] é algo que vem por padrão em aplicações com spring security, é algo que impossibilita o chamado de métodos DELETE, PUT e POST.

Para fazer o spring gerar um token CSRF é necessário criar um endpoint para pegar o Token da atual da sessão e utilizar nas requisições desejadas, é ideal que esse endpoint seja separado dos outros, então por exemplo em uma aplicação de dois tipos de endpoints como de uma livraria com autores e livros, deve-se criar um terceiro somente para autenticação. Para isso deve-se fazer o seguinte:
![[Pasted image 20260119230747.png]]
- Na primeira linha está criando o endpoint para pegar o token
- Na segunda é criada a função para obter o token, dá a ela o retorno do tipo `CsrfToken` que é um retorno padrão do spring security, depois o nome do método e o parâmetro que é chamado de token e é do tipo `CsrfToken` que também é um tipo adicionado por padrão pelo spring security.
- Depois, apenas é retornado o parâmetro.




