## Funções

A sintaxe de funções do kotlin é semelhante a do java, porém, no kotlin a palavra chave é "fun" e deve ser informado o tipo de retorno da função em um local diferente do que no java:
![[Pasted image 20260408215948.png]]

Funções também podem ser escritas como expressões:
![[Pasted image 20260408220012.png]]

Também é possível não retornar algo em específico, para informar que uma função não precisa retornar algo basta usar a palavra chave "Unit" ou deixar a parte onde seria informado o tipo do retorno em branco:
![[Pasted image 20260408220901.png]]

Ou, sem "Unit"
![[Pasted image 20260408220918.png]]


## Variáveis
No kotlin as variáveis podem ser criadas com "val" ou com "var". Sendo, respectivamente uma imutável e mais segura, e a outra que pode mudar várias vezes no código, sendo menos segura mas oferecendo mais liberdade.

elas podem ser declaradas definindo o tipo ou deixar que a linguagem detecte o tipo automaticamente:
![[Pasted image 20260408221703.png]]

Ou deixando o kotlin definir o tipo automaticamente:
![[Pasted image 20260408221733.png]]



## Classes
No kotlin, a criação de classes é bem simples e seus atributos podem até mesmo serem passados em sua criação:
![[Pasted image 20260408222811.png]]

para adicionar métodos basta utilizar as chaves e criar os métodos  dentro do escopo da classe:
![[Pasted image 20260408222921.png]]

E tem até mesmo como utilizar o "Override" que tinha no java, um bom exemplo de uso é para o método `toString()`:
![[Pasted image 20260408223030.png]]


para criar objetos a partir de uma função é bem simples, basta colocar em uma variável e colocar os atributos:
![[Pasted image 20260408223117.png]]


e para chamar métodos também é simples, basta chamar o objeto e com um ponto chamar o nome do método:
![[Pasted image 20260408223155.png]]


### Herança

Classes no kotlin, pode padrão são `Final` o que faz com que não permite a herança. Para mudar isso basta marcar a classe com a palavra-chave `Open`:
![[Pasted image 20260408223511.png]]


Aproveitando que já está sendo falado de herança, para realizar a mesma basta utilizar o `:`, dessa maneira:
![[Pasted image 20260408224536.png]]

![[Pasted image 20260408224516.png]]


