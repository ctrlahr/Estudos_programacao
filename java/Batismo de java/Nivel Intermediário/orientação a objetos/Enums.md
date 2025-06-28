Enums podem ser criados no java como se fossem classes, porem, quando está sendo criado, tem que selecionar a opção de enum ao invés de java class ou interface por exemplo, enums são utilizados como tipos de dados, na declaração de uma variável, deve-se passar como o tipo de dado dela o nome dado ao nosso enum:

*Criação de um enum*
![[Pasted image 20250620151748.png]]
- É uma boa prática utilizar todos os atributos em caixa alta.

*Criação de uma variável com o tipo enum:*
![[Pasted image 20250620152034.png]]

*Atribuição do tipo enum no construtor se referenciando a variável do tipo enum:*
![[Pasted image 20250620152127.png]]


Enums são principalmente utilizados quando o desenvolvedor tem a plena certeza que o que estiver dentro do enum não vai mudar por exemplo dias da semana e meios de pagamento.
Cada enum só pode ser um enum, então por exemplo, não dá pra criar um enum pra armazenar os dias da semana e as formas de pagamento, deve-se criar um enum especifico de dias da semana e de métodos de pagamento.
Também é possível utilizar variáveis dentro dos enums.

