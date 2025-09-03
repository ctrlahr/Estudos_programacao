## Stack(Pilha)
A estrutura pilha segue um conceito chamado "LIFO", que significa "last in, first out", e isso, por que o ultimo dado que for adicionado ao topo da estrutura da pilha será o primeiro a sair. É como uma pilha de pratos. 

#### Como aplicar a pilha em python
Em python especificamente a estrutura de pilha pode ser aplicada nas listas e podemos utilizar do método `append` para adicionar novos itens ao topo de nossa pilha e do método `pop` para removermos itens do topo da nossa lista:
```
from typing import List
stack: List[str] = []

stack.append("A")
stack.append("B")
stack.append("C")

print(stack)

stack.pop()
```
- Neste código começamos criando uma lista e por questões de boas práticas, na criação da mesma já definimos o tipo de dado que ela irá armazenar que nesse caso é String. 
- são adicionados dados a lista, sendo eles, A, B e C.
- depois é removido o ultimo item adicionado a esta lista, nesse caso, o "C"


Quando queremos um loop para iterar sobre nossa lista, se for feito da maneira tradicional, os dados não virão na ordem que é desejada para uma estrutura de pilha, eles virão da base para o topo mas o que é desejado é ao contrário, do topo para a base, para isso podemos utilizar do slice(fatiamento), onde não escrevemos o inicio e o fim de até onde queremos iterar sobre a ista, dizendo assim que queremos percorrer ela por inteira, depois adicionamos o passo, e colocamos esse passo negativo, indicando que queremos que a iteração aconteça de trás para frente ao invés do convencional:
```
for item in stack[::-1]:
	print(item) 
```

Outra maneira de iterar sobre a lista da maneira certa é utilizando o laço while e um método  `copy`, é feita uma cópia da lista original e essa cópia é armazenada em uma variável e utilizando do while é possível falar que enquanto tiver algo nessa cópia da lista continuará mostrando o valor que foi retirado pelo pop:
```
stack_copy = stack.copy()

while stack_copy:
	item = stack_copy.pop()
	print(item)
```

Uma forma melhor de realizar está cópia é com o método de uma biblioteca chamada copy, o "deepcopy", que permite realizarmos cópias de dados mutáveis como listas. Para isso basta apenas que a biblioteca seja importada e no lugar de `copy`, é utilizado deepcopy na hora de armazenar a cópia em uma variável:
```
from copy import deepcopy

stack_copy = deepcopy(stack)
```

