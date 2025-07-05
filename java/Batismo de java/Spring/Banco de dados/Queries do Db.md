

## SELECT

O `SELECT` é utilizado para selecionar algo de uma tabela ou do banco de dados mesmo, sua sintaxe é `*` se quiser selecionar tudo de uma tabela ou especificar uma coluna da tabela para selecionar:
![[Pasted image 20250705003740.png]]

Ou selecionando uma coluna específica:
![[Pasted image 20250705003805.png]]


## INSERT
O `INSERT` é utilizado para inserir algo a uma tabela, é necessário passar a tabela que terá algo inserido nela e entre parênteses deve ser passado as colunas que vão ser preenchidas com os dados, depois passa-se os dados:
![[Pasted image 20250705004620.png]]


## ALTER TABLE
O `ALTER TABLE` é utilizado para alterar alguma propriedade de uma tabela selecionada, operações como criar novas colunas, apagar colunas, etc:
![[Pasted image 20250705010158.png]]

#### ADD COLUMN
Adiciona uma nova coluna a tabela selecionada, além de que deve estar abaixo do alter table indicando a tabela: 
![[Pasted image 20250705010249.png]]
- é necessário passar o nome da  coluna e o tipo dela, nesse caso a coluna se chama rank e recebe o tipo varchar.