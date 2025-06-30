Finals são as constantes do java então são elas que serão utilizadas para dizer que não é desejado que o valor de algo mude como um atributo de uma classe ou até mesmo um método inteiro.

## Métodos Final
Métodos final são métodos que não podem ser sobrescritos, ele é único do tipo dele.
Para declarar um método final basta trocar o `public` por `final`:
![[Pasted image 20250627234142.png]]

## Atributos final
Atributos final são simplesmente atributos que não podem mudar, é a forma de utilizar constantes no java, para criar um atributo final basta colocar a palavra chave `final` no começo, antes da declaração do tipo da variável:
![[Pasted image 20250627234859.png]]

também é possível criar atributos final que não necessitam ser inicializados já na classe, para isso não pode ter um construtor vazio apenas um construtor `allArgs`:
![[Pasted image 20250630154502.png]]
Dessa forma, os atributos são definidos na chamada da classe(no construtor).
Além de que atributos final não podem ter setters já que como são finals não é possível altera-los, dessa forma, apenas getters conseguem ser utilizados em atributos final.


## Classes Final
Usar o final em classes faz com que elas não possam mais ser extendidas nem podem extender ou implementar.
Para criar uma classe final basta trocar o `public` por `final`:
![[Pasted image 20250628000743.png]]
