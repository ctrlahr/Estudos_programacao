ffStreams são uma forma de simplificar operações de busca, filtragem, ordenação, etc. 
Dentro da stream existem inúmeros métodos que facilitam operações que muitas vezes seriam mais demorados como um método `filter()` para filtrar itens específicos de uma lista ou até mesmo o método `sorted()` para automaticamente fazer uma ordenação da lista.

Para usar as streams é necessário usar o `.stream()` para depois passar a operação desejada.

Operações em streams podem ser intermediárias ou finais:

## Operações intermediárias
As operações intermediárias são aquelas que retornam um novo stream para que possa ser encadeado. Então no exemplo do método `sorted()` é retornado uma nova stream mas dessa vez uma stream organizada conforme foi pedido e posteriormente, a mesma deve ser retornada por um método final como o `forEach()`


*Operações intermediárias:*
### `filter()`
O método filter é utilizado para filtrar algo de uma lista, podendo ser para no exemplo de ninjas mostrar apenas os ninjas que são da aldeia da folha. Nesse caso é necessário utilizar o método filter e passar como parâmetro do método um predicate que vai indicar exatamente o que deve ser filtrado:
![[Pasted image 20250724123212.png]]



### `Sorted()`
O método sorted serve para ordenar a lista da forma desejada. Existem dois métodos sorted, um que precisa de um comparator e outro que não precisa.
No caso do método sorted sem o comparator ele pega a lista passada não importando seu tamanho e ordena por comparação, comparando por exemplo os dois primeiros ninjas da lista e vendo qual ninjas tem a primeira letra do nome que vem primeiro no alfabeto, e a mesma coisa pra os outros elementos da lista e é a mesma coisa para listas de números, o que muda é que ao invés de comparar a letra ele compara qual número vem primeiro.


*Comparando números inteiros:*
![[Pasted image 20250724130050.png]]
- Nesse caso a ordenação é feita por idade, então é comparado a idade dos ninjas e a lista é ordenada de forma crescente.
- deve ser passado parâmetros e utilizar de [[Expressões lambda]] para passar o que deverá acontecer, nesse caso simplesmente é usado o método compare de Integer para comprar as idades dos ninjas.

*Comparando Strings:*
![[Pasted image 20250724132846.png]]
- Nesse caso a ordenação é feita por ordem alfabética e para isso como `String` não apresenta um método compare é necessário comparar com o método `compareTo`, dessa forma, passando o nome do primeiro ninja e utilizando o método para comparar com o nome do segundo ninja, tendo apenas isso de diferença com a ordenação de números.


### `Map()`
Utilizado para transformar cada elemento da stream aplicando uma função a ele, podendo ser uma função de multiplicação para multiplicar cada valor de uma lista de inteiros por 2 por exemplo ou até mesmo para iterar sobre uma lista de nomes e mostrar cada um:
![[Pasted image 20250725131003.png]]

Tem uma diferença entre usar a seta de lambda expression(`->` ) para usar o method reference(`::`)
A seta dos métodos lambda é utilizada em casos que o método não existe, em casos que por exemplo seja necessário criar um método rápido para somar números entre si, nesse caso, será necessário o uso de expressões lambda:
![[Pasted image 20250725132559.png]]

Já o method reference é utilizado quando o método que deve ser chamado já existe seja em outra classe ou até mesmo no java:
![[Pasted image 20250725132944.png]]
- Nesse exemplo foi necessário utilizar o map para converter primeiramente `Ninja` para string para que a operação `toUpperCase` seja utilizada.


## Operações terminais
Operações terminais são aquelas em que se retorna um resultado que não é uma nova stream, então por exemplo, o método `forEach()` é utilizado para retornar um valor final, nesse caso, retornar algo para cada elemento da stream.


*Operações terminais:*
### `forEach()`
O método `ForEach()`é utilizado geralmente para printar todos os elementos de uma lista mas seguindo o exemplo da lista de ninjas no mesmo código em que foi feita a filtragem para mostrar apenas os ninjas que são de konoha, aquele código não retornaria nada, por que nenhuma operação de retorno está sendo executada, é ai que entra o `forEach`, o qual foi utilizado para iterar sobre cada item da lista filtrada e printar cada um apenas com uma linha de código sem precisar criar todo um loop para isso:
![[Pasted image 20250724123251.png]]


### `Max()`
O método max encontra o maior elemento da stream, é uma operação terminal que retorna um Optional, isso significa que ele também precisa de algo caso não tenha nada.
Para comprar algo como por exemplo comprar e ver quem é o ninja mais velho de uma lista de ninjas é necessário criar um comparador e esse comparador é criado assim; `Comparator.comparing()`, é como dizer "compare esses ninjas baseado nisso"
Passando como parâmetro o que vai ser utilizado para comparar.
![[Pasted image 20250725134613.png]]
- Nesse exemplo está sendo utilizado o comparator para comparar a idade dos ninjas passando o tipo de dado, nesse caso, o tipo de dado é a classe `Ninja` e passando o método, nesse exemplo, o método para obter a idade.
- Depois somente é utilizado do `orElse` para retornar null.
- Já fora da stream é necessário retornar já que não tem um método de retorno nessa stream, então é printado a stream.



### `Collect()`
O método collect é utilizado dentro das streams para poder coletar o que foi feito na camada intermediária e transformar em um elemento do tipo collection. Ele funciona com base no `Collector` passado, então se o collector passado informar que a stream deve ser um set ela será um set, a mesma coisa para maps, lists e entre outros:
![[Pasted image 20250726121710.png]]
- Nesse exemplo está sendo utilizado uma stream para transformar a lista de Model para DTO então está com o `map()` usando o método map do mapper para justamente fazer essa conversão 
- Com o collect é transformado toda a stream em uma lista para ser retornada.




## Uma outra explicação
