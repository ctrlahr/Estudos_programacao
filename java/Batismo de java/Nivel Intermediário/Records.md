Records são basicamente classes imutáveis, então será criado um objeto de um record mas os dados desse objeto não vão poder ser alterados.
Records automaticamente  já inclui getters, hashcode, toString e equals o que faz com que não seja necessário a criação de um getter, setters não podem ser utilizados nos records justamente pela sua imutabilidade, então seus valores nunca irão mudar. 
records são muito utilizados no Spring quando o intuito é trabalhar com DTO's ou para POJOs(classes simples do java que não dependem de frameworks ou de bibliotecas específicas para funcionar.)

*record:*
![[Pasted image 20250717095213.png]]

*classe main:*
![[Pasted image 20250717095245.png]]

É visível a criação de um objeto record é muito parecida com um construtor.