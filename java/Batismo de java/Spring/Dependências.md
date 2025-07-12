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
O `flyway` é utilizado para se ter um sistema de versionamento para o banco de dados, dessa forma tornando mais fácil algumas operações, funciona basicamente como um git mas para banco de dados.

Para usar o versionamento de banco de dados é necessário criar uma pasta para guardar essas alterações que forem feitas, ela deve ser criada na pasta de `resources` e dentro da pasta resources é legal que exista também uma outra pasta chamada migrations e dentro dessa pasta terão as versões do banco de dados.
Cada arquivo de versão tem uma nomenclatura especifica, eles sempre começam com um "V" e depois o número da versão seguido de dois underlines, o nome da versão e a extensão `.sql`: 
![[Pasted image 20250705134516.png]]

E posteriormente, deve ser escrito nesse arquivo a alteração que vai acontecer no banco de dados:
![[Pasted image 20250705134950.png]]
Dessa forma, toda e qualquer alteração que seria feita feita direto no painel do banco de dados agora pode ser feita na IDE.

Além disso, também é necessário dar a autorização de execução, nesse caso o flyway precisa ser ativado, deve ser passado onde ele vai trabalhar e também é necessário falar para o flyway que se já existir algo no banco de dados a migration deve ser feita para o que já existe, então se algo já existe, a migration deve ser feita para a tabela já existente e isso tudo no `aplications.properties` que cuida das permissões e configurações do projeto:
