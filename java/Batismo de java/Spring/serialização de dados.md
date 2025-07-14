 Quando se está trabalhando com banco de dados, normalmente é necessário que tenha uma forma de o usuário conseguir se comunicar e realizar [[Queries do Db||queries]] do banco de dados sem estar dentro do painel administrativo do mesmo. Isso é feito na [[Padrão de projeto||arquitetura por camadas]] com o arquivo de `Service` que cuida da parte lógica do projeto. 


## Serialização com todos os dados de uma tabela

Para fazer com que mostre todas as informações de uma tabela específica o primeiro passo é definir que o nosso arquivo é o arquivo de `service`, ou seja, informar para o spring que tal arquivo é o arquivo que vai tomar conta da parte lógica do código, isso é feito por meio de uma anotação que é a anotação `@Service`:
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




## Serialização com um dado informado por Id da tabela

Também é possível realizar a serialização de dados especificando um id. Para isso é necessário utilizar o método [[Dependências||findById()]]. criando a lógica dentro do arquivo de service deve ser declarado um método depois de realizar a injeção de dependência do `Repository`.
Esse método tem que receber um parâmetro e deve retornar o que está na tabela de acordo com o id:
![[Pasted image 20250707111022.png]]
- Nesse caso primeiro é criada um método que retorna o tipo `NinjaModel` por que `NinjaModel` o retorno deve ser da classe onde está a tabela, se fosse desejado que retornasse de outra tabela deveria estar o nome de outra tabela. 
- Depois, utilizando dos [[Optional]] e atribuindo o resultado do `findById` a variável correspondente. O optional é utilizado nesse caso para dizer que se o usuário passar um id que não está correspondente a nenhum ninja não retornará nenhum erro por que é "opcional".
- Por ultimo, retorna-se o resultado mas é utilizado um método que é o `orElse()` esse método é utilizado para se não encontrar algo, então nesse caso se encontrou o ninja no Db ele irá retorna-lo, se não ele retornará null.

Após isso, o outro processo é realizado no `controller`, deve ser criado um método que vai também retornar um tipo `NinjaModel`, é necessário passar um parâmetro e o retorno será de `ninjaService` que deve ter sido posteriormente injetado e é  utilizado o método criado anteriormente:
![[Pasted image 20250707112327.png]]
- Nesse caso o id está sendo passado via URL mas também pode ser passado pelo Frontend, etc. Para passar o id pela URL é necessário criar um path variable, para isso, na rota é criado um subdomínio que servirá apenas para passar o id, o mesmo deve ser passado entre chaves e tem que ser o mesmo nome do parâmetro.
- No parâmetro deve ser utilizada a notação de `@PathVariable` para dizer que esse parâmetro deve subir para o URL.
- Por fim é retornado o ninja com id informado por meio do método anteriormente criado.

Esse código retorna algo parecido com isso:
![[Pasted image 20250707113138.png]]



## Serialização inversa
A serialização inversa no Spring e com o [[Dependências||JPA]] é feita por meio do método `save()`, ele é utilizado para realizar uma requisição POST onde serão passadas informações para o banco de dados, diferente de requisições do tipo GET que pegam informações do Db. Dessa forma será feita uma serialização inversa dos dados, onde o usuário passará as informações e essas informações serão repassadas para o Db.

Exemplo:

*Service:*
![[Pasted image 20250711132016.png]]
- Nessa imagem é criado um método público com o propósito de utilizar o método save,
- primeiro define o retorno desse método como `NinjaModel` já que o que será retornado deve ser um modelo do ninja
- como parâmetro, para evitar colocar, nome, idade, email, etc, é passado a classe `NInjaModel` por completo já que a mesma apresenta esses atributos
- como retorno, apenas é utilizado o método `save` com parâmetro do método `criarNinja`


*Controller:*
![[Pasted image 20250711132817.png]]
- no método da requisição para criar um ninja é utilizado uma anotação de `@RequestBody` no parâmetro desse método, essa anotação é utilizada para indicar que um parâmetro de método deve ser vinculado ao corpo da requisição HTTP, basicamente instrui o sprig para deserializar automaticamente o conteúdo do corpo da requisição geralmente JSON para um objeto java.
- depois, apenas é retornado o método criado por meio da injeção de dependência do service e passado como parâmetro o próprio parâmetro da função de criar ninja.