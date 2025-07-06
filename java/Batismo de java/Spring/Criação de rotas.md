Para criar novas rotas no Spring é necessário utilizar algumas anotações além de estar em um arquivo específico, em uma classe especifica.

- É na classe controller que as rotas são gerenciadas, então antes de criar as rotas deve existir o arquivo controller que vai gerenciar as rotas do projeto.

- Depois, é necessário utilizar das anotações `@RestController` que um componente que lida com requisições HTTP e retornando dados diretamente para o corpo da resposta e também fala ao spring que a classe que está anotada é uma classe controladora e `@RequestMapping` é como um mapa detalhado que guia requisições HTTP para método java correto na aplicação, permitindo assim grande flexibilidade na definição de URLs e tipo de requisição. Com o `@RequestMapping` é possível também, passar subdomínios, dessa forma os nomes de algumas rotas podem ser iguais a outras:
		![[Pasted image 20250706164242.png]]
		Dessa forma, todos que estiverem dentro dessa classe vão seguir sempre o caminho de `missoes` e só depois a rota que foi passada.

- Depois, usa-se a anotação `@GetMapping` para definir a rota onde algo vai aparecer, então por exemplo, um método que retorna uma mensagem de boas vindas vai aparecer na rota `/BoasVindas`, a anotação `@GetMapping` faz uma requisição `GET`, diferente por exemplo da anotação `@PostMapping` que faz requisições `POST`

![[Pasted image 20250627155836.png]]

Esse código, retorna isso no navegador:
![[Pasted image 20250627160123.png]]



## `@GetMapping`
`@GetMapping` vem da requisição GET que é utilizada para quando se quer mostrar ou dar algo para o usuário, o usuário pede algo específico e é retornado para ele conforme foi pedido. 

Exemplo:
![[Pasted image 20250706165228.png]]


## `@PostMapping`
`@PostMapping` vem de um tipo de requisição chamada de POST, ela é utilizada para quando o usuário vai mandar algo para o código ou para o banco de dados. Então casos em que por exemplo, o usuário vai cadastrar alguém em um aplicativo de cadastros, etc.

Exemplo:
![[Pasted image 20250706164905.png]]


## `@PutMapping`
`@PutMapping` vem da requisição PUT que é utilizado para alterações, sendo assim, utilizado para atualizar completamente um recurso existente e até mesmo consegue criar um novo recurso se o mesmo ainda não existir.

Exemplo:
![[Pasted image 20250706164924.png]]


## `@DeleteMapping`
`@DeleteMapping` vindo da requisição DELETE, ele realiza operações de deletar algo, é utilizado para remover recursos do servidor, removendo um recurso especificado e podendo retornar status de confirmação.

Exemplo: 
![[Pasted image 20250706165647.png]]
