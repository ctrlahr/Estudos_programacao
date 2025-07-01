Queues são basicamente o inverso das stacks, elas tem a característica de FIFO(first in first out). Então o primeiro elemento sempre vai ser o primeiro a sair.
Sendo o primeiro elemento a `head` da fila e o ultimo elemento a `tail` da fila.
Queues fazem parte da família das linked lists, sendo assim, na sua criação é necessário utilizar uma declaração de liked lists:
![[Pasted image 20250701132455.png]]

podendo também ser declarada sem ser passado seu tipo:
![[Pasted image 20250701132947.png]]
Permitindo assim utilizar as queues com diversos tipos de dados na mesma queue.


## Métodos das queues

#### add()
Adiciona um elemento um elemento em fila, então o primeiro que foi adicionado sempre será o primeiro, já o segundo ficará em segundo, assim por diante.
![[Pasted image 20250701133246.png]]

![[Pasted image 20250701133255.png]]

#### poll()
O método poll é utilizado para remover o head da queue.
![[Pasted image 20250701133641.png]]

![[Pasted image 20250701134325.png]]
#### peek()
Assim como no stack, é utilizado para "Espiar" quem é o primeiro da fila e retorna isso.
![[Pasted image 20250701134402.png]]

![[Pasted image 20250701134351.png]]

#### isEmpty()
Verifica se a queue está vazia
![[Pasted image 20250701134619.png]]

![[Pasted image 20250701134626.png]]


