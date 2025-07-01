Os relacionamentos entre tabelas são feitos utilizando anotações. Elas devem ser colocadas em cima do atributo que recebe a primeira característica, então por exemplo, `@ManyToOne` em cima de um atributo `missoes` e dentro da classe `ninjaModel` diz que podem ter muitos ninjas para uma só missão.
![[Pasted image 20250701015833.png]]

E é o contrário para a outra tabela, nesse caso, a tabela de missões:
![[Pasted image 20250701020045.png]]

### @OneToMany
Pode ser traduzido para um para muitos.

### ManyToOne
Traduzido para muitos para um.


## Foreign key
É com as foreign keys que é possível ligar duas tabelas, no spring tem algumas formas de se utilizar ela.

*Explicar quando eu souber mais...* 

