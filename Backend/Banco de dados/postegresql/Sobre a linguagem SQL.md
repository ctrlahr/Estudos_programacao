## Subconjuntos da linguagem SQL
##### *DDL* (Data Definition Language)
↪São comandos que estaremos utilizando com o propósito de estar criando, alterando ou excluindo uma tabela.
- *CREATE TABLE;*
	↪ Utilizado quando queremos criar uma nova tabela em nosso banco de dados:
```
CREATE TABLE nome_da_tabela (
	coluna1 tipo_de_dado restrições opcionais,
	coluna2 tipo_de_dado restrições opcionais,
	...
);

Ou com um exemplo real...

CREATE TABLE clientes (
	id SERIAL PRIMARY KEY,
	nome VARCHAR(100) NOT NULL,
	idade INT,
	email VARCHAR(100) UNIQUE
);
```
Melhor explicação em [[Tipos de dados de atributos]] 

- *ALTER TABLE*;
	↪ É utilizada para modificar a estrutura de uma tabela existente, podendo modificar, adicionar ou até mesmo remover colunas:
```
ALTER TABLE nome_da_tabela
ADD coluna_nome tipo_de_dado restrições_opcionais; # Adcionando uma coluna

ALTER TABLE nome_da_tabela
DROP COLUMN coluna_nome; # Removendo uma coluna

ALTER TABLE nome_da_tabela
ALTER COLUMN coluna_nome TYPE novo_tipo_de_dado; # Alterando uma coluna

Ou com um exemplo real...

ALTER TABLE clientes
ADD telefone VARCHAR(15); # Adcionando uma coluna

ALTER TABLE clientes
DROP COLUMN idade; # Removendo uma coluna

ALTER TABLE clientes
ALTER COLUMN nome TYPE TEXT; # Alterando uma coluna
```
	
- *DROP TABLE*;
	↪ É utilizado para excluir uma tabela já existente no banco de dados, removendo a tabela e todos os dados contidos nela permanentemente, sendo necessário ser utilizado com cautela visto que ao utilizar este comando os dados não podem ser recuperados a não ser que exista um backup dos mesmos:
```
DROP TABLE nome_da_tabela;

Ou com um exemplo real...

DROP TABLE clientes;
```


##### *DML* (Data Manipulation Language)
↪São comandos que vamos utilizar a fim de manipular os dados, seja inserindo novos registros a uma tabela existente, deletando registros existentes de uma tabela ou modificar dados existentes em uma tabela
-  *INSERT*;
	↪ É utilizado quando queremos inserir algo a uma tabela, quando queremos adicionar novos registros a uma tabela já existente.
```
INSERT INTO nome_da_tabela (coluna1, coluna2, coluna3, ...)
VALUES (valor1, valor2, valor3, ...)

Ou Com um exemplo real...

INSTERT INTO clientes (nome, idade, email)
VALUES ('joão', 30, 'joao@exemple.com');
```

-  *DELETE*;
	↪ É utilizado para removermos registros existentes de uma tabela
```
DELETE FROM nome_da_tabela
WHERE condição;

Ou com um exemplo real...

DELETE FROM clientes
WHERE idade > 60;
```

-  *UPDATE*;
	↪ É utilizado para atualizarmos registros já existentes de uma tabela.
```
UPDATE nome_da_tabela
SET coluna1 = valor1, coluna2 = valor2, ...
WHERE condição;

Ou com um exemplo real...

UPDATE clientes
SET idade = 31
WHERE nome = 'joão';
```


##### *DQL* (Data Query Language)
↪ São os comandos que utilizaremos com propósito de consultar os dados armazenados em um banco de dados, permitindo que os usuários recuperem informações específicas do banco de dados de forma estruturada e eficiente.
- *SELECT*
	↪ É utilizado com o propósito de obtermos informações:
```
SELECT atributos_de_uma_tabela FROM nome_da_tabela

Ou com um exemplo real...

SELECT nome, idade FROM clientes;
```



*Ver mais depois...*
##### *DCL* (Data Control Language)
↪ Aborda mais as partes de administração dos usuários no banco de dados, basicamente controlamos o acesso aos dados e definimos permissões em um banco de dados.
- *CREATE USER*;
	↪

- *ALTER USER*;
	↪


##### *DTL* (Data Transaction Language)
- *BEGIN TRANSACTION*;
	↪

- *COMMIT*;
	↪

- *ROLLBACK*;
	↪