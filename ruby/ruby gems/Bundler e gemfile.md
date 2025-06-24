
##### Oque é um bundler
Bundler é basicamente uma ferramenta que nos ajuda a gerenciar nossas gems. Ele serve para garantir que todas as versões que você tem instaladas no seu projeto também estarão instaladas no mesmo projeto mas em um computador diferente. Sendo de grande interesse quando vamos fazer um deploy, ou seja. Colocar nossa aplicação final no ar para que os usuários finais utilizem, pois com o bundler tudo irá funcionar corretamente no servidor. Ou seja, basicamente o bundler faz com que tudo que fucionava no seu computador funcione no servidor também, evitando erros.

O bundler ajuda também quando temos gems incompatíveis entre si.


##### Gemfile
No gemfile nós escrevemos uma lista das gems que iremos utilizar no projeto


##### Como criar e usar o bundler
- Primeiro criamos um arquivo dentro do nosso projeto chamado gemfile e dentro desse projeto nós adicionamos as seguintes coisas:
```
source 'https://rubygems.org' => Site onde o gemfile irá buscar as gems(geralmente o site oficial do rubygems

ruby '3.3.3' => Versão que será utilizada do ruby

gem 'enumerate_it' => gem que queremos utilizar
gem 'rails', '4.2.0' => Maneira de escolher uma versão especifica de uma gem
```

- Depois abrimos o terminal na pasta do nosso projeto e rodamos o comando `bundle install` ou simplesmente `bundle`
- após isso nós podemos criar nosso arquivo ruby e botar o código do nosso projeto. 
- dentro do arquivo do projeto nós temos que usar o comando `require 'bundler/setup'` e logo a baixo para inicializarmos o bundler o `bundler.require`. É válido falar que se todo esse passo a passo apenas acontece se você estiver criando um projeto do absoluto zero mas por exemplo se o rails estiver sendo utilizado todo esse processo acontece automaticamente.