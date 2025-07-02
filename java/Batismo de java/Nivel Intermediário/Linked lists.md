Ao contrário das ArrayLists, as LInkedLists são muito mais otimizadas para operações de remoção e colocação de elementos, sendo bem mais performáticas e uteis para algorítimos em que se tem muitos elementos para se trabalhar.

Linked lists funcionam por meio de ponteiros, ou seja, cada item na linked list está apontando para o próximo item, por exemplo, em uma lista com "Naruto, Sasuke e Sakura" o Naruto está apontando para o Sasuke e o Sasuke está apontando para a Sakura, sendo assim, se um novo item for adicionado por exemplo na frente do Naruto, o que vai mudar será apenas o ponteiro do Naruto que antes apontava para o Sasuke e agora vai apontar para o Kakashi.
![[Pasted image 20250701192738.png]]
Linked lists nem sempre são sequenciais, por exemplo o Kakashi nesse caso poderia ter uma referência de memória de `@403` enquanto o Naruto tem uma referência de memória de `@101` e mesmo assim estar na frente do Naruto justamente por que o que vale é o ponteiro. Justamente por isso as linked lists são de alta performance quando o assunto são operações de remoção e alocação. 
E por isso também que as linked lists são horríveis em tarefas de pesquisa, pois elas não tem índices, então essas tarefa se torna milhares de vezes mais complexa.

Linked lists são chamados de listas encadeadas por que o que encadeia elas, o que cola elas são ponteiros de cada elemento que sempre aponta para o próximo elemento da lista.
Por que os ponteiros se "linkam" entre si.


## Criação de linked lists
A criação das linked lists é bem padrão, praticamente da mesma forma como listas comuns são passadas, podendo ser com a declaração do tipo delas e sem:

###### Com tipo
![[Pasted image 20250701200956.png]]

###### Sem tipo
![[Pasted image 20250701201031.png]]


## Quando escolher Linked lists no lugar de array lists
As linked lists devem ser utilizadas no lugar das array lists principalmente quando é necessário lidar com grande volume de dados pois as linked lists tem um desempenho maior que as array lists quando esse é o assunto.


##### Qual a diferença de uma lista encadeada para um array list
- Principalmente, ArrayLists são ótimas quando a tarefa é pesquisar algo dentro delas, algum elemento ou algo do tipo, mas sendo péssimas e extremamente anti-performáticas quando o quesito é operações de colocação e remoção de itens, isso pode ser explicado mais detalhadamente [[Array list||aqui]].
- Já em contra partida, Linked lists são horríveis para pesquisar algo, diferente das Array lists.


Para pegar elementos por índices em linked lists, é necessário utilizar o método `get()`, dessa forma: 
![[Pasted image 20250702155605.png]]
Sendo necessário, colocar dentro de um print para fazer algo com o retorno deste método.