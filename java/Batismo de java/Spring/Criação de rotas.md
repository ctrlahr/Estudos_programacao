Para criar novas rotas no Spring é necessário utilizar algumas anotações além de estar em um arquivo específico, em uma classe especifica.

- É na classe controller que as rotas são gerenciadas, então antes de criar as rotas deve existir o arquivo controller que vai gerenciar as rotas do projeto.

- Depois, é necessário utilizar das anotações `@RestController` que um componente que lida com requisições HTTP e retornando dados diretamente para o corpo da resposta e também fala ao spring que a classe que está anotada é uma classe controladora e `@RequestMapping` é como um mapa detalhado que guia requisições HTTP para método java correto na aplicação, permitindo assim grande flexibilidade na definição de URLs e tipo de requisição.

- Depois, usa-se a anotação `@GetMapping` para definir a rota onde algo vai aparecer, então por exemplo, um método que retorna uma mensagem de boas vindas vai aparecer na rota `/BoasVindas`, a anotação `@GetMapping` faz uma requisição `GET`, diferente por exemplo da anotação `@PostMapping` que faz requisições `POST`

![[Pasted image 20250627155836.png]]

Esse código, retorna isso no navegador:
![[Pasted image 20250627160123.png]]



