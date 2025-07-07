Quando se está trabalhando com banco de dados, normalmente é necessário que tenha uma forma de o usuário conseguir se comunicar e realizar [[Queries do Db||queries]] do banco de dados sem estar dentro do painel administrativo do mesmo. Isso é feito na [[Padrão de projeto||arquitetura por camadas]] com o arquivo de `Service` que cuida da parte lógica do projeto. 

Para fazer isso o primeiro passo é definir que o nosso arquivo é o arquivo de `service`, ou seja, informar para o spring que tal arquivo é o arquivo que vai tomar conta da parte lógica do código, isso é feito por meio de uma anotação que é a anotação `@Service`:
![[Pasted image 20250706230405.png]]


é necessário também realizar a conexão do `Service` com o `Repository` e isso é feito criando um atributo do tipo do `Repository`:
![[Pasted image 20250706230438.png]]
- Nesse caso o `Repository` se chamava `NinjasRepository` então o tipo que esse atributo tinha que ser era do tipo `NinjasRepository`


Depois é necessário criar um método referente a querie desejada, isso é feito por meio do [[Dependências||JPA]] que está sendo implementado pelo `Repository`, dessa forma, para acessar tudo do JPA basta utilizar do atributo que está sendo utilizado para linkar o `Service` com o `Repository`: 
![[Pasted image 20250706233143.png]]

também é necessário injetar a dependência do `Service` no `Controller`, semelhante com o que foi feito na injeção de dependência do `Repository` no `Service`, para isso basta criar um atributo e um construtor assim como foi feito no `Service`: 
![[Pasted image 20250706233445.png]]

O ultimo passo é apenas utilizar o método criado no `Service` na rota correspondente:
![[Pasted image 20250706233631.png]]
- Nesse caso a rota lista todos os ninjas no Db e o método tem essa utilidade.

Um erro é bem comum quando se está trabalhando com serialização, esse erro é o loop de serialização, ele ocorre quando uma tabela se referência a outra por meio de um foreign key causando um loop realmente, ele pode ser facilmente resolvido por meio de uma anotação chamada `@JsonIgnore`, a mesma deve ser colocada na tabela que está sendo ligada:
![[Pasted image 20250706234924.png]]

Se tudo isso for feito ao entrar na rota deverá retornar algo semelhante a isso: 
![[Pasted image 20250706235411.png]]