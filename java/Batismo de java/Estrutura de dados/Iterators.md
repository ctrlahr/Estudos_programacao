Iteradores no java são uma interface que permitem percorrer collections elemento por elemento, é como um cursor que aponta para cada um dos elementos um de cada vez.
Iteradores são importantes por que por exemplo em um sistema de remoção de itens fora do estoque se faz necessário verificar se o item existe o que é uma tarefa mais fácil e limpa com iterators.

Iterators tem vários métodos, os principais são:
- `hasNext()` - Verifica se ainda há elementos
- `next()` - Retorna o próximo elemento e avança o cursor
- `remove()` - Remove o último elemento retornado por `next()`

Para criar um iterator é necessário fazer assim:
![[Pasted image 20251013094147.png]]

Dessa forma está sendo criado um iterador e atribuindo ele a uma collection específica que nesse caso é um ArrayList de pessoas em uma fila.

Iterators podem ser utilizados também para iterar sobre uma lista  com o `While`, por meio de seus métodos:
![[Pasted image 20251013094425.png]]

Esse código imprime todos os nomes da lista assim como também é feito pelo `ForI` mas é mais como uma alternativa.


### vantagens importantes

*Remoção segura*
Durante a iteração, se for utilizado dos iteradores é possível realizar a remoção segura de elementos:
![[Pasted image 20251013094920.png]]

Porém, para operações de remoção foi introduzido um atalho no Java 8, que foi o `removeIf()`.
O `removeIf` é um método que simplifica bastante algumas operações:
![[Pasted image 20251013095631.png]]
Nessa código está sendo removido todos os números impares de uma lista.

No código do próprio `removeIf` está sendo utilizado um iterator mas não há necessidade de você mesmo utilizar já que ele simplifica para você.

Abaixo está uma comparação do mesmo código porém, um utiliza do iterador puro e o outro do método `removeIf`:
![[Pasted image 20251013095939.png]]


Algo importante de citar é que para listas existe um iterador específico que é o `ListIterator`, ele permite navegar nos dois sentidos(frente e trás) e até mesmo adicionar elementos durante uma iteração:
![[Pasted image 20251013100143.png]]
