
## Herança

A herança serve para facilitar um trabalho que levaria muito tempo, tendo uma classe mãe e criando classes filhas que vão herdar caracteristicas da classe principal, por exemplo. Se Existe uma classe ninja com atributos de nome, aldeia, idade, etc, e existe uma classe uchiha, essa classe uchiha vai ter atributos específicos ou até mesmo métodos específicos da classe uchiha mas ela vai herdar nome, idade, aldeia, etc da classe mãe ninja.

Como é feita a herança em java:
![[Pasted image 20250617235817.png]]
- Assim, na criação de um novo objeto, o objeto só terá a função como no exemplo `AtivarSharingan` se for do tipo uchiha e não do tipo ninja.
	![[Pasted image 20250618000043.png]]


## Interfaces
Interfaces são quase como janelas, é possível acessa-la, então, seria possível, abrir ela, olhar o que está dentro, pegar o que é necessário e ir embora quantas vezes quiser.
Diferentemente das classes, as interfaces não permitem a criação de objetos, por que as interfaces só estão para ser usadas de forma rápida, a interface não é um molde. 

Para criar interfaces no java, é necessário criar um novo arquivo, nesse novo arquivo é dado o nome e posteriormente selecionada a opção interface.

Para criar métodos em interfaces não é necessário criar com `void main nomeDoMetodo(){}` pois interfaces são realmente como janelas, onde somente usaremos ela para pegar algo de dentro dela, então só é necessário declarar a variável:
![[Pasted image 20250618222430.png]]

Depois, como não é possível criar objetos de classes, pode-se criar uma classe para herdar tudo da interface e de uma classe que for selecionada. Para acessar as funções da interface é necessário utilizar a palavra-chave "implements" e passar o nome da interface.
Depois, como os métodos apenas foram declarados na interface, agora é necessário que eles sejam declarados novamente e passado uma função para eles, isso se faz com o [[Polimorfismo| @override]]:
![[Pasted image 20250618223957.png]]

- Interfaces não conseguem extender de outras classes mas conseguem extender de outras interfaces.
- Interfaces não conseguem ser implementadas, ou seja, não é possível criar objetos a partir de interfaces, é necessário que elas sejam implementadas por outras classes ou estendidas por outras interfaces.
- Interfaces por padrão já são públicas, por isso não é necessário na criação de seus métodos falar que eles são públicos.


A herança múltipla acontece quando são utilizadas múltiplas interfaces em uma só classe, isso é feito da seguinte forma:
![[Pasted image 20250627001723.png]]

