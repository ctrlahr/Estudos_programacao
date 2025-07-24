Streams são uma forma de simplificar operações de busca, filtragem, ordenação, etc. 
Dentro da stream existem inúmeros métodos que facilitam operações que muitas vezes seriam mais demorados como um método `filter()` para filtrar itens específicos de uma lista ou até mesmo o método `sorted()` para automaticamente fazer uma ordenação da lista.

Para usar as streams é necessário usar o `.stream()` para depois passar a operação desejada.

### `filter()`
O método filter é utilizado para filtrar algo de uma lista, podendo ser para no exemplo de ninjas mostrar apenas os ninjas que são da aldeia da folha. Nesse caso é necessário utilizar o método filter e passar como parâmetro do método um predicate que vai indicar exatamente o que deve ser filtrado:
![[Pasted image 20250724123212.png]]


### `forEach()`
O método `ForEach()`é utilizado geralmente para printar todos os elementos de uma lista mas seguindo o exemplo da lista de ninjas no mesmo código em que foi feita a filtragem para mostrar apenas os ninjas que são de konoha, aquele código não retornaria nada, por que nenhuma operação de retorno está sendo executada, é ai que entra o `forEach`, o qual foi utilizado para iterar sobre cada item da lista filtrada e printar cada um apenas com uma linha de código sem precisar criar todo um loop para isso:
![[Pasted image 20250724123251.png]]


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