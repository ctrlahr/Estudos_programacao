Polimorfismo é a capacidade de objetos de diferentes classes sejam tratados como se fossem da mesma classe, isso é alcançado principalmente por heranças e interfaces, permitindo com que métodos existentes de classes ou até mesmo de interfaces sejam sobrescritos para fornecer diferentes comportamentos em diferentes classes.



## Anotações
- Tudo que tem o "@" na frente é chamado de anotação


#### @Override
A anotação Override é capaz de sobrescrever um método, por exemplo, em um programa há uma classe uchiha que herda de ninja, a classe mãe ninja tem um método padrão chamado "ataqueEspecial", esse método printa uma mensagem no terminal falando "Esse é meu ataque especial, eu sou um ninja" mas a classe uchiha tem que ter um ataque especial diferente, afinal, são uchihas, então é utilizado do @Override a fim de sobrescrever o método "habilidadeEspecial" e mudar sua mensagem para algo do tipo "Esse é meu ataque especial, um ataque de fogo, eu sou um uchiha":

*Classe Ninja:*
![[Pasted image 20250619140925.png]]

*Classe Uchiha:*
![[Pasted image 20250619140939.png]]

a anotação override é uma boa prática, ela não é obrigatória mas é uma boa prática,  mas também serve para evitar erros.