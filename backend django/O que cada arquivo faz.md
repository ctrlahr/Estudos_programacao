## __init__
É um arquivo vazio que indica que o diretório é uma pacote python, ele permite o python reconhecer o diretório como um pacote para que seja possível importar módulos dele

## asgi
Utilizado para configurar o servidor ASGI que é uma evolução do WSGI que suporta operações assíncrona, útil para aplicações que precisam lidar com conexões de longa duração.

## settings
Contem as configurações do arquivo python, define coisas como a lista de aplicativos instalados, configurações do banco de dados. idioma, etc. Controla como o projeto vai se comportar em diferentes ambientes.

## url
Responsável por mapear URLs para views(Funções ou classes que processam uma requisição e retornam uma resposta), é por ele que se é definida as rotas do seu projeto.

## wsgi
Ajuda o django a servir os arquivos criados por ele, utilizado para configurar o servidor WSGI que é um padrão para servir aplicativos python na web. Utilizado mais frequentemente quando está implantando o projeto em um servidor de produção.

## manage
permite interagir com o projeto django de diversas maneiras, como iniciar o servidor de desenvolvimento.