## Funções e do que se tratam as pastas que o flutter cria

- As utilizadas para codar são as pastas lib e test que realiza testes de unidade
- Cada uma das outras pastas são referente ao código para a plataforma selecionada como por exemplo a pasta web que é utilizada para o flutter na programação web
- A pasta buid é basicamente pra onde vão os binários ou seja as coisas que foram construídas ou seja, quando por exemplo nós criamos nossa aplicação o apk dela vai para essa pasta
- Os arquivos ".metadata" e ".packages" eles tem a função de situar o flutter onde as coisas externas que ele utiliza estão
- O "analysis_options.yaml" serve para colocarmos regras para seguirmos quando estivermos escrevendo nosso código
- "pubspec.lock" e "pubspec.yaml" que vão nos auxiliar na hora de trabalharmos com dependências externas. Nós mexemos no "pubspec.yaml" mas não mexemos no pubspec.lock até por que o pubspec.yaml irá gerar o pubspec.lock


## básico do flutter

#### Oque são widgets?
Widgets são basicamente uma parte da tela que ou pode representar toda tela do celular ou então partes dela. No flutter tudo é um widget até mesmo o aplicativo padrão. 


### Estrutura padrão flutter
#### Criando um aplicativo
Primeiramente para podermos criar uma aplicação com flutter nós temos que ter um widget que seja responsável pela tela inteira. Para podermos jogarmos esse widget na tela do celular nós utilizamos a função `runApp(...)` que vem importada de `package:flutter/material ou cupertino.dart`

Para criarmos uma aplicação inicial nós precisamos estender/herdar de widget. Então, criamos uma classe para ser a classe para o aplicativo e estendemos ou seja, herdamos widget dela: 
`class MyApp extends Widget {}`

Normalmente precisaríamos criar uma classe e herdar de element e de create widget mas o flutter facilita esse processo, basta apenas então quando nós formos criar a classe do nosso aplicativo nós herdarmos de "StatelessWidget" que é basicamente uma classe auxiliar para criar um widget. Utilizando dessa classe nós não precisaremos de uma parte de criação de elemento oque facilita muito nosso processo