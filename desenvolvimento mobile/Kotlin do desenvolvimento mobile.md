## Código padrão
![[Pasted image 20260414224212.png]]
Sempre que um novo projeto é criado no android studio, no arquivo kotlin principal sempre tem algumas linhas de código e cada uma tem um propósito:

![[Pasted image 20260414224236.png]]
Cria a tela principal do aplicativo, basicamente cria a classe `MainActivity` e faz essa classe herdar de `AppCompatActivity` o que traz funcionalidades prontas do android.



![[Pasted image 20260414224424.png]]
É o método que roda assim que a tela é criada



![[Pasted image 20260414224517.png]]
O `super.onCreate` chama o `OnCreate` original do android por causa da palavra chave `Super`. Isso serve para realizar preparações antes de executar definitivamente o aplicativo, já que o `OnCreate` original tem funções para restaurar o estado anterior da tela, preparar o sistema de layout, configurar o ciclo de vida da tela, etc.

E o `enableEdgeToEdge` faz o conteúdo do aplicativo ocupar a tela inteira.



![[Pasted image 20260414225116.png]]
Essa seção de código serve para estar resolvendo um problema causado pelo `enableEdgeToEdge` que é que ao ativar essa função o conteúdo do aplicativo cobrirá de uma parte da tela até a outra, até mesmo atrás da barra de status que fica no canto superior do celular, esse código resolve isso, pegando as medidas das barras que variam de celular para celular(por isso não pode ser um número exato) e aplica um espaçamento inteiro usando as medidas das barras, assim, impedindo de algo sumir atrás da barra de status.



## Conectar XML com o código

Para conectar um elemento da interface(do XML) no código kotlin é necessário primeiramente [[XML| mudar o ID do componente no XML]]
Também é necessário ativar essa função no `Build.Gradle.kts` do Module :app. no Build.Gradle deve-se escrever a configuração que permitirá com que possa haver a conexão entre XML e kotlin:

Dentro da caixa de configuração de `Android`:
![[Pasted image 20260414222956.png]]

Dentro do arquivo kotlin:
![[Pasted image 20260414223846.png]]

Somente esse código é responsável por tornar possível, o que ele faz é que `binding` fica como a variável que será utilizada para acessar os elementos visuais da tela(Botões, textos, etc.) assim, por meio dessa variável, será possível acessar por exemplo `Text` de uma caixa de texto e mudar o texto pelo próprio código.
E abaixo, em `setContentView` é onde é definido qual layout será exibido na tela que nesse caso usa-se `binding.root` para informar que deve-se mostrar tudo do layout.