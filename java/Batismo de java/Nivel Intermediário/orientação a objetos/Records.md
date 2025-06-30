Records são um tipo especial de classe que facilitam em 100x o processo de criação de uma classe. O processo de se criar um record é muito fácil também:
![[Pasted image 20250630155930.png]]
Records por padrão já entregam construtores já feitos, getters e setters, etc.
Records devem ser principalmente utilizados quando é garantido que não será alterado, então por exemplo, 

- Records não podem ser abstratos nem ter métodos abstratos.
- Todos os atributos de records são por padrão final, não permitindo assim a alteração dos mesmos, dessa forma, também não tem setters.
