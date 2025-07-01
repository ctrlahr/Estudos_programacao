Stack é uma estrutura de dado em que o primeiro que entra é o ultimo que saí, basicamente se por exemplo, a palavra "oi" entra em uma stack ela está ocupando a posição 1 da stack. Quando algo novo é inserido a essa stack automaticamente este item se torna o item na posição 1 e o item anteriormente na posição 1 desce para a posição 2, dessa forma também, quando for para remover itens da stack o item na posição 2 será removido depois do item na posição 1.


## Como criar stacks
Para criar stacks é necessário utilizar da palavra chave reservada `Stack`, dessa forma, utiliza dos generics para definir o tipo daquela stack:
![[Pasted image 20250630213812.png]]

Mas também é possível criar stacks sem informar explicitamente o seu tipo, permitindo assim criar um stack que armazena tipos de dados diferentes:
![[Pasted image 20250630214132.png]]


## Métodos das stacks

#### push()
O método push é utilizado para adicionar elementos a stacks:
![[Pasted image 20250630220216.png]]

#### pop()
Utilizado para tirar algo da lista, nesse caso, ele tira o primeiro elemento da stack:
![[Pasted image 20250630220315.png]]

#### peek()
Utilizado para verificar qual o próximo elemento da pilha, dessa forma retornando o ultimo valor que foi colocado nessa stack:
![[Pasted image 20250630220413.png]]

ou para já pegar o retorno e printar:
![[Pasted image 20250630220446.png]]

#### size()
Retorna o tamanho da pilha, a quantidade de elementos: 
![[Pasted image 20250630220513.png]]

Ou para já pegar o retorno e mostrar na tela:
![[Pasted image 20250630220538.png]]