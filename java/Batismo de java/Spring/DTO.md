DTO's são cópias de entidades em um banco de dados, não tendo acesso ao banco de dados e não tendo a responsabilidade de ser uma entidade. Eles oferecem uma camada a mais de proteção e segurança para sua aplicação.
São utilizados para tirar a responsabilidade da entidade, dessa forma criando uma camada que se comunicará diretamente com o service no lugar da entidade. Com essa alteração se torna possível alterar o controller para criar novas colunas por exemplo mas antes deve ser criado no DTO referente a tabela uma cópia:

*DTO:*
![[Pasted image 20250714125728.png]]

*Controller:*
![[Pasted image 20250714125744.png]]

Ele tem tudo que o `model` tem mas sem as anotações de banco de dados já que o mesmo não tem a obrigação de ser uma tabela do banco de dados:
![[Pasted image 20250714130449.png]]

Para o spring saber que o que está no DTO é o que está no controller é necessário fazer um mapeamento, esse mapeamento é feito com o arquivo `mapper`, primeiro deve ser criada uma classe mapper e essa classe recebe uma anotação de `@Component` para que o spring detecte que aquela classe é um componente, é um mapper mesmo:
![[Pasted image 20250714202208.png]]

*Mapper:*
Existem duas formas de fazer o mapeamento do controller para o DTO, uma delas é utilizando a anotação `@Mapper`  onde é preciso baixar uma dependência para o projeto, e a outra fazendo manualmente, criando uma função que faz esse mapeamento.

*@Mapper:*


*Manualmente:*
Primeiro é necessário mapear o que está no `NinjaModel`para o `DTO`:
![[Pasted image 20250714132006.png]]

Depois, é feito o caminho inverso, deve ser mapeado do `DTO` para o `NinjaModel`:
![[Pasted image 20250714132328.png]]

Após o processo do mapeamento é necessário trocar o que antes era `NinjaModel` por `NinjaDTO`como por exemplo no arquivo de service onde os métodos retornavam `NinjaModels`, para isso é necessário injetar a dependência do mapper no service:
![[Pasted image 20250714133113.png]]

depois de injetada a dependência do mapper, o próximo passo é alterar as menções do `NinjaModel`:

*Antes:*
![[Pasted image 20250714200353.png]]

*Depois:*
![[Pasted image 20250714200951.png]]
- No código é convertido o objeto do tipo `NinjaDTO` para um `NinjaModel` para que as operações passadas no `NinjaModel` como definir automaticamente um id funcionem corretamente.
- Depois, é utilizado o método save para salvar no banco de dados passando como parâmetro o objeto do tipo `NinjaModel`.
- E por fim é convertido novamente para um DTO e retornado para o usuário.