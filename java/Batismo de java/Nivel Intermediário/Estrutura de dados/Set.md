

#### Diferenças dos sets para as listas
- O set na maioria das vezes apenas vai ser utilizado quando o intuito é ignorar itens duplicados dentro da lista por que ele não permite itens duplicados. 
- Sets não possuem ordenação, dessa forma, seus elementos aparecem em uma ordem aleatória. Sets também não possuem índices, dessa forma, sets também não possuem nodes, eles são um caso a parte e não se igualam em forma de pesquisa as `linkedLists` ou as `arrayLists`.

## HashSet
Hash sets são utilizados quando a necessidade é criar uma lista sem itens duplicados e sem ordem específica também.


Para criar HashSets essa é a estrutura:
Com definição explicita de tipo e deixando o set para suportar apenas um tipo de dado:
![[Pasted image 20250703083400.png]]

Sem definição explícita de tipo, deixando o set para armazenar qualquer e vários tipos de dados:
![[Pasted image 20250703083443.png]]


### Métodos

#### AddAll()
O método `addAll()` é utilizado para passar uma collection inteira como parâmetro para transformar ela em um set:
![[Pasted image 20250703085213.png]]

#### remove()
O `remove()` do set não funciona como o de uma lista justamente pela particularidade de não ter ordenação, dessa forma, o que deve ser passado no remove para remover um item é  o nome do item:
![[Pasted image 20250703085904.png]]




## TreeSet
Tree Sets são principalmente utilizados quando a necessidade é ter uma lista sem itens duplicados mas em ordem sequencial referente ao tipo de dado no set, por exemplo, para strings ele é organizado em ordem alfabética enquanto para inteiros o set é organizado em ordem do menor para o maior:

![[Pasted image 20250703090857.png]]



## LinkedHashSet
O linkedHashSet faz a mesma coisa de um HashSet, não deixando duplicatas de algum item mas ele deixa na ordem que o item foi colocado na lista, por ordem de inserção: 
![[Pasted image 20250703091230.png]]