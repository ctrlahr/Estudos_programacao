Para transformar classes em entidades em um banco de dados primeiro a classe além dos atributos convencionais dela, também deve apresentar um atributo id que não tem necessidade de estar no construtor mas é necessária ela existir nos atributos.
![[Pasted image 20250627205814.png]]


E para de fato transformar uma classe em uma entidade é necessário o uso de uma anotação chamada `@Entity`. Mas, para usar essa anotação é necessária a instalação de uma dependência para trabalhar com banco de dados, que nesse caso é a[[Dependências|| Spring Data JPA]].
![[Pasted image 20250627210643.png]]
Então cada coluna da tabela vai ser um atributo da classe.
Também é possível dar um nome a tabela, isso é feito por meio da anotação `@Table`:
![[Pasted image 20250627211016.png]]
- Assim, é passado entre parênteses o nome da tabela, sendo uma boa prática o nome sempre começar com tb e ser escrito todo em minúsculo em snake case(Com underline).

É necessário também, informar ao java como que o `id` deve ser preenchido automaticamente, para isso é necessário o uso de mais uma anotação chamada `@Id` e a `@GeneratedValue` para gerar um número automaticamente:
![[Pasted image 20250627211913.png]]



