Deque é uma estrutura de dado do java que faz parte das collections. Seu nome significa double-ended-queue ou fila de duas pontas. 
Por ser uma estrutura de duas pontas as deque's permitem com que elementos sejam inseridos e removidos em ambas extremidades de forma eficiente.



*Métodos das deque's:*

- `addFirst()` ou `offerFirst()`: Adiciona ao inicio da deque.
- `addLast()` ou `offerLast()`: Adiciona ao final da deque.
- `removeFirst()` ou `pollFirst()`: Remove o primeiro item da deque.
- `removeLast()` ou `pollLast()`: Remove o último item da deque.
- `peekFirst()`: Consulta o primeiro item da deque.
- `peekLast`: Consulta o último item da deque.


Existem duas formas de implementar a deque ao código java, são elas por `ArrayDeque` ou [[Linked lists| `LinkedList`]]:


*ArrayDeque:*
ArrayDeques são mais rápidos na maioria das operações e tem uma melhor performance para operações de deque.
Porém apresentam algumas desvantagens como não ser possível armazenar valores `null` e podem escapar memória se o array estiver parcialmente vazio.

Vale ressaltar que o acesso por índice não é suportado nativamente por ArrayDeques.


para utilizar essa implementação basta informar na criação da deque:
![[Pasted image 20251201222636.png]]




*LinkedList:*
LinkedLists é uma implementação que se destaca para algumas operações o que a torna melhor em alguns casos. 
No geral as LinkedLists nos deque permitem elementos `null`, não tem a necessidade de redimensionar, implementam nativamente `List`, o que permite o acesso por índice e é melhor para interações de remoção frequentes já que utiliza o sistema de nós.
Porém, assim como as ArrayDeques as LinkedLists também tem desvantagens, as principais são que usam mais memória e tem uma performance inferior para a maioria das operações de deque.

Vale ressaltar as complexidades de algumas operações como a de remoção das pontas que tem uma [[Complexidade de algorítimo | notação]] de [[Complexidade de algorítimo| O(1)]] e a de acesso por índice que apresenta uma notação de [[Complexidade de algorítimo| O(n)]].



Para utilizar essa implementação basta informar na criação da deque também:
![[Pasted image 20251201222625.png]]



No geral as diferentes implementações se adaptam para diferentes cenários.
Enquanto os `ArrayDeque` são melhores quando se prioriza a performance, necessita de elementos `null`, precisa do uso típico de deque.
Os LinkedLists são melhores quando se precisa de valores `null`, precisa acessar elementos por índice e necessita de iteradores que removem elementos durante uma iteração.