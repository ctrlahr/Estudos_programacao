## Spring web


## Spring Data JPA
Sua sigla significa "java persistence API", a spring data JPA é uma dependência que permite com que o dev trabalhe com banco de dados SQL no projeto spring.
É uma abstração(Maneira de simplificar um processo) que permite trabalhar com banco de dados.

##### ORM
A dependência do JPA traz junto o ORM que uma de suas funcionalidades é atuar como um scanner que vai escanear a classe pedida e vai passar seus atributos para o banco de dados, basicamente traduzindo o código java em código que o banco de dados entenda.
Para utilizar dessa funcionalidade do ORM é necessário extender o `JpaRepository` em alguma interface ou classe como uma interface de repository que vai conectar o banco de dados ao código:
![[Pasted image 20250704133005.png]]
- é necessário passar a classe que o JPA quer que o ORM fique escaneando
- Também é necessário passar o tipo de dado do ID da classe.

O ORM funciona quase que como um tradutor da linguagem que está sendo utilizada para a linguagem do banco de dados. Ele vai mapear toda a classe passada para ele e vai traduzir para o DB.
![[Pasted image 20250704134700.png]]




## LomBok
O Lombok é utilizado para facilitar a criação de construtores, então, é possível criar construtores `AllArgs` e `NoArgs` de forma muito mais fácil, a anotação do lombok apenas precisa estar em cima da classe:
![[Pasted image 20250703110638.png]]

o lombok também cria getters e setters, basicamente da mesma forma, usando a anotação de `@data` em cima da classe:
![[Pasted image 20250703111003.png]]



## Bancos de dados
Para trabalhar com bancos de dados é necessário baixar a dependência relativa ao banco de dados e adicionar ao pom.xml no caso do maven, segue um exemplo com o H2: 
![[Pasted image 20250704143724.png]]