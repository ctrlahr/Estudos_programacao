Collection é uma interface que é implementada por outras interfaces, sendo elas as interfaces por exemplo de listas ou até mesmo de queue ou de set, então collections é um objeto que representa um grupo de outros objetos, é uma estrutura que permite armazenar, organizar e manipular uma coleção de elementos.
A interface collection é a raiz que define alguns métodos básicos como `add()`, `remove()`, `size()` e `isEmpty()`. 
No geral, as collections são uma interface que oferece estruturas de dados para armazenar e manipular grupos de objetos de forma eficiente.
É por essa característica de ser uma interface que quando feito um print e passando a própria lista, queue, etc, que é retornado o que está dentro da lista e não sua referencia de memória, por que dentro da interface collection existe já um método `toString()` que faz o que teria que ser feito manualmente pelo dev.

Existe uma pequena arvore básica para explicar as implementações das collections:
![[Pasted image 20250701202245.png]]
