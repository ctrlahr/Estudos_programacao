Listas são basicamente arrays com super poderes, são arrays que não são estáticos e tem métodos específicos.


## Diferença de listas para arrays
Arrays são estáticos, ou seja, não alteram de tamanho, para alterar o tamanho de um array é necessário ir na declaração do array e alocar mais espaços na memória manualmente.
Diferentemente das listas que não são estáticas, podendo assim aumentar e diminuir de tamanho.


Diferente dos arrays que quando passado no print o próprio array sem índice nenhum mostrava a referência de memória daquele array, as listas tem a capacidade de mostrar o seu conteúdo, assim, não é necessário a criação de um laço de repetição para mostrar o conteúdo da lista:

*Com For:*
![[Pasted image 20250629154437.png]]

![[Pasted image 20250629154446.png]]


*Com listas:*
![[Pasted image 20250629154218.png]]

![[Pasted image 20250629154231.png]]


## Criação de listas
A criação de listas no java é bem simples, é necessário utilizar a palavra chave `List` e entre diamantes(`<>`) passar o tipo de dado dessa lista, depois, passa-se o nome da lista e atribui tudo isso a `new` e a palavra chave `ArrayList<>()`:
![[Pasted image 20250629153831.png]]

## Métodos da listas

#### Adicionar elementos
Para adicionar elementos a listas basta apenas passar o nome da lista e utilizar o método `.add()` e dentro do parentese passar o que deve ser adicionado a lista:
![[Pasted image 20250629153940.png]]

#### Remover elementos
Para remover elementos de uma lista é necessário utilizar o método `remove()` e passar dentro dos parênteses o nome exato que deve ser removido:
![[Pasted image 20250629154956.png]]


#### Trocar elementos
Para trocar elementos na lista deve-se utilizar o método `set` e passar como parâmetro primeiro o index de onde está o que deve ser trocado e pelo que deve ser trocado:
![[Pasted image 20250629155416.png]]
- nesse caso, está trocando o elemento que está no index 4 por "Hashirama Senju".


#### tamanho da lista
O método para ver o tamanho da lista é o `size()`, simplesmente passando o nome da lista e utilizando o método:
![[Pasted image 20250629155701.png]]

Mas é necessário fazer algo com o retorno do tamanho, então colocar em um print é uma boa opção:
![[Pasted image 20250629155737.png]]

#### Pegar index específicos
Para isso deve utilizar o método `get()`, dessa forma, passando o index dentro dos parênteses:
![[Pasted image 20250629160307.png]]

