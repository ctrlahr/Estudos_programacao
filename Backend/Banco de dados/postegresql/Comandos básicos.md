
## Inserindo registros na tabela
Para inserirmos algo em uma tabela já criada do nosso banco de dados nós utilizamos o comando "insert", dessa forma:
```
INSERT INTO nome_da_tabela(coluna1, coluna2, ...) VALUES(valor1, valor2, ...);
```

## Atualizando registros na tabela
Para atualizarmos registros já existentes de uma tabela utilizamos o "update":
```
UPDATE nome_da_tabela SET coluna1 = valor1, coluna2 = valor2, ...
WHERE condição;
```

É importante lembrar que o uso do "where" é opcional, entretanto, quando não usamos ele nós vamos atualizar todos os registros presentes naquela tabela então por exemplo, uma tabela de funcionários que queremos atualizar o salário:
*Sem utilizar o where*
```
UPDATE employees
SET salary = 5000;
```
- Esse código irá atualizar o salário de todos os funcionários da tabela "employees" para 5000

*Utilizando o where*
```
UPDATE employees
SET salary = 5000;
WHERE department = 'sales';
```
- Já esse, com a utilização do where nós estaremos atualizando o salário apenas dos funcionários do departamento "sales"

## Removendo registros de uma tabela
Para estarmos removendo um registro nós utilizamos o "delete" e passamos o nome da tabela e a condição:
```
DELETE FROM nome_da_tabela WHERE condição;

ou 

DELETE FROM nome_da_tabela
WHERE condição;
```

Lembrando que a utilização do where aqui se mostra também opcional mas sem o uso dele nós ao executar o comando estaremos removendo todos os registros da tabela:
*Com where*
```
DELETE FROM employees;
```
- Esse comando remove todos os registros da tabela "employees"

*Com where*
```
DELETE FROM employees
WHERE departament = 'sales';
```
- E esse comando remove registros de funcionários que pertencem ao departamento "sales"

## Alterando partes da tabela
Para podermos mudar o nome de alguma coluna nós utilizamos o "alter table" e o rename:
```
ALTER TABLE Nome_da_tabela
RENAME COLUMN Nome_da_coluna TO Novo_nome_da_coluna
```

## Selecionando registros
Para podermos consultar as informações que já estão inseridas em nossa tabela nós utilizamos o "select" e passamos o nome da tabela:
```
SELECT coluna1, coluna2, coluna3, ... FROM nome_da_tabela;
```

Mas se caso quisermos consultar todas as colunas da nossa tabela utilizamos o "*", assim:
```
SELECT * FROM nome_da_tabela;
```


## Definindo chaves primárias
temos duas formas para a definição de uma chave primária e são elas:

Passando o comando "primary key" na criação do atributo:
```
CREATE TABLE products (
	id int PRIMARY KEY
)
```

E a outra forma é quando já temos a tabela criada e queremos definir depois a chave primária, fazemos isso usando o "alter table" e adicionando uma constraint([[constraints]]). Para isso fazemos assim:
```
ALTER TABLE products
ADD CONSTRAINT nome_da_constraint PRIMARY KEY(nome_do_atributo);
```

## removendo chaves primárias
 Para isso usamos também o "ALTER TABLE", dessa forma:
```
ALTER TABLE products
DROP CONSTRAINT products_pk;
```


## Natural keys X Surrogate keys
Uma natural key é um campo que já existe na tabela:
```
CREATE TABLE persons (
	name VARCHAR(60),
	cpf VARCHAR(11) PRIMARY KEY,
	...
);
```
- Essa é uma chave natural pois esse campo(cpf) que naturalmente já estaria nessa tabela pois estamos criando uma tabela de pessoas e como chave única nós já temos uma existente que nesse caso é o cpf já que o mesmo é único para cada pessoa

Já uma surrogate key ela é uma constraint que criamos apenas com o propósito de darmos uma chave única para aquele atributo da tabela como por exemplo um "id" ou algo do tipo.
```
CREATE TABLE persons (
	name VARCHAR(60)
	id INT PRIMARY KEY,
	...
);
```

 