Construtores são como moldes para as classes, ou seja, quase como moldes para um molde.
Existem dois tipos de construtores, sendo eles os construtores:

*NoArgs constructor:* um construtor que vem vazio e não necessariamente recebe algum argumento, então é um construtor que por padrão não necessita receber algum argumento

*AllArgs constructor:* É um construtor que é preenchido com todos os atributos da classe.

Por padrão o java já cria um construtor, é criado um construtor sem argumentos ou um construtor do tipo "NoArgs". É por isso que na criação de um novo objeto é passado `new NomeDaClasse()`:
![[Pasted image 20250620125922.png]]
esse parêntese vazio indica um construtor NoArgs, já se fosse um construtor AllArgs esse espaço dos parênteses deveria estar preenchido

Criar um construtor `NoArgs` é bem simples:
![[Pasted image 20250620130559.png]]

Já um construtor `AllArgs` é um pouco mais complexo:
![[Pasted image 20250620131424.png]]
- É criado o construtor e dentro dos parênteses passa-se os argumentos, quase como parâmetros de uma função, é necessário informar seu tipo e também, é necessário que esses atributos já existam na classe:
		![[Pasted image 20250620131601.png]]
- Depois, é necessário referenciar e falar que o atributo nome vai receber o que for passado no construtor, isso é feito por meio do `this.` que acessa o atributo que for informado, por exemplo `this.nome` está acessando o atributo nome, e depois, com o sinal de atribuição, informar que o atributo nome vai receber o que for passado no construtor.


Existe um atalho extremamente útil que é o `Ctrl+N`, ele abre essa tela:
![[Pasted image 20250620132438.png]]
Nessa tela é possível criar tudo isso que já está ai, para criar construtores, criar construtores quando eles tem muitos atributos é algo muito trabalhoso, mas com esse atalho se torna muito fácil. Basta apenas selecionar os atributos que você quer que façam parte do construtor e apertar "Ok".



### Construtores para subclasses
Para ter construtores em subclasses é preciso informar que os atributos que vão ser pegos da classe mãe são da classe mãe, para isso é usado o `super();`, dessa forma:
![[Pasted image 20250626212135.png]]

e para um construtor noArgs:
![[Pasted image 20250626212422.png]]

