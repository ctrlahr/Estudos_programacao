Para criar uma classe nova, é necessário criar um novo arquivo, uma nova classe e colocar os valores da 

classe dentro do escopo da classe, sem criar uma função main.
![[Pasted image 20250615134509.png]]


é simplesmente dessa forma que é criado o que uma classe vai receber

## O que é um objeto
Na **programação orientada a objetos (POO)**, um **objeto** é uma **instância de uma classe**. Ele representa **algo do mundo real ou conceitual** que possui atributos ou propriedades que descrevem o estado do objeto e métodos ou comportamentos que definem o que o objeto pode fazer. 


## Criando uma novo objeto dessa classe
Para criar um novo objeto pense como se faz para chamar um scan, é criado um novo objeto da classe scan, dessa forma, para criar-se um novo objeto da classe criada anteriormente basta isso:
![[Pasted image 20250615140528.png]]

Depois, atribuí-se os valores a respectivos objetos:
![[Pasted image 20250615140603.png]]


## Classes abstratas e métodos abstratos

### Classes abstratas
Classes abstratas, também conhecidas como super classes servem para padronizar o código, para forçar todas as sub-classes que nascerem a partir de uma determinada classe a seguir um padrão determinado.

##### Diferenças de uma classe abstrata para uma classe padrão
1. Classes abstratas não podem ter objetos criados a partir dela, não podem ser instanciadas como as [[Herança e interfaces|| Interfaces]] que também não podem ser instanciadas. Elas apenas são criadas para serem extendidas/herdadas.
2. Classes abstratas tem a capacidade de ter métodos abstratos.

##### Diferenças classe abstrata para interfaces
1. Toda vez que um método é criado em uma interface ele é obrigatoriamente abstrato.
2. Toda vez que uma interface é criada não é permitido apenas a declaração da variável e depois, quando ela for implementada dar o valor a variável, toda variável criada em interfaces precisam obrigatoriamente já serem declaradas com um valor pois tudo é automaticamente final.
 

##### Como tornar uma classe abstrata
é bem simples, basta apenas depois da declaração de pública, usar a palavra chave `abstract`:
![[Pasted image 20250625143739.png]]
Assim, estará tornando uma classe normal em uma classe abstrata.



### Métodos abstratos
Métodos abstratos são métodos que são declarados sem corpo:
![[Pasted image 20250625144825.png]]

eles devem ser instanciados na classe que herdar a super classe.