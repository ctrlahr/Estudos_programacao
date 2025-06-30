Generics em java são uma forma de deixar o código mais seguro e flexível, permitindo a criação de classes e métodos que funcionam com diferentes tipos de dados sem perder a verificação de tipos. 
Um bom exemplo é imaginar uma caixa, sem generics, essa caixa aceita qualquer coisa então, é possível colocar uma maça, um livro, etc, dessa forma, quando alguém for pegar algo da caixa não sabe exatamente o que vai encontrar, com os generics é possível especificar o tipo daquela caixa, por exemplo, uma caixa de maçãs.
Em geral, são os generics que são utilizados nas listas para definir o tipo delas, então em uma declaração `List<String> lista = new ArrayList<>();` está sendo criada uma lista que só armazena tipos `String`. 

Generics também podem ser utilizado em classes.