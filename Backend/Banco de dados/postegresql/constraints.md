Uma constraint são como regras que podemos definir em uma tabela para garantirmos a integridade dos dados, usamos elas para assegurar que os dados inseridos na tabela atendam a determinados critérios, como por exemplo a constraint primary key que basicamente define um atributo de uma tabela como chave primária.
Podemos definir uma assim:
```
CREATE TABLE teste (
	id int PRIMARY KEY
)
```

Algo legal de ser pontuado é que um atributo pode receber mais de uma constraint:
```
email VARCHAR(60) NOT NULL UNIQUE,
```
- Nesse exemplo as constraints de "email" são "NOT NULL" e "UNIQUE"

As principais constraints são:

| Constraint  |                                                                                                             Explicação                                                                                                             |
| :---------: | :--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------: |
|  NOT NULL   |                                                Garante que uma coluna não pode conter valores nulos, ou seja, esse registro se torna obrigatório já que o campo não pode ser nulo.                                                 |
|   UNIQUE    |                                                            garante que todos os valores em uma coluna sejam únicos em toda a tabela, não permitindo valores duplicados                                                             |
| PRIMARY KEY |                                                     Basicamente combina o "NOT NULL" e "UNIQUE" já que uma chave primária não pode ser nula e tem que ser única para a tabela.                                                     |
| FOREIGN KEY |                                        Estabelece uma relação entre duas tabelas garantindo que o valor em uma coluna corresponda a valores existentes em uma outra coluna de outra tabela                                         |
|    CHECK    | Faz com que possamos definir uma condição para que os dados devem atender para serem inseridos ou atualizados, como por exemplo quando queremos armazenar apenas pessoas maiores de 18 anos, ai nesse caso utilizariamos o "CHECK" |
|  EXCLUSION  |                                                               Garante que em um conjunto de colunas não existam duas linhas que satisfaçam uma determinada condição                                                                |
|   DEFAULT   |                                                                                  Define um valor padrão para uma coluna se nada for especificado                                                                                   |

## NOT NULL

## UNIQUE

## PRIMARY KEY

## FOREIGN KEY
Uma foreign key como foi explicado na tabela de forma mais superficial, é uma constraint que referencia ou liga tabelas entre si, podemos fazer isso de duas formas:

*Na criação da tabela*
Quando queremos já definir uma foreign key na criação da tabela nós utilizamos o "REFERENCES", dessa forma:
```
CREATE TABLE departaments(
	id SERIAL PRIMARY KEY,
	name VARCHAR(100) NOT NULL
);

CREATE TABLE users(
	id SERIAL PRIMARY KEY,
	name VARCHAR(100) NOT NULL,
	dapartaments_id INT REFERENCES departaments(id)
);
```
- Estamos utilizando do "REFERENCES" para definir a ligação entre esses atributos de duas tabelas diferentes

*Com a tabela já existente*
Nesse caso vamos utilizar do "ALTER TABLE" com "FOREIGN KEY" e o "REFERENCES", dessa forma:
```
ALTER TABLE users
ADD CONSTRAINT fk_departaments
FOREIGN KEY (departaments_id)
REFERENCES departaments(id);
```
- Aqui estamos criando uma constraint com o nome de fk_departaments
## CHECK

## EXCLUSION

## DEFAULT

## Constraints DEFERRABLE