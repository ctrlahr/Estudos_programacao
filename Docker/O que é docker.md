Docker é uma forma de se disponibilizar o aplicativo, site, produto no geral para outras pessoas de forma que funcione da mesma forma que funciona em sua máquina para evitar o famoso "Na minha máquina funciona".
Docker é um serviço de virtualização isso significa que a aplicação consiga funcionar corretamente independente do ambiente em que a mesma se encontre. através do serviço de virtualização poderá ser feito o deploy da aplicação contendo todas as dependências necessárias.
A forma como isso é feito é por meio de containers, o docker coloca a aplicação e suas dependências dentro de um container onde o container será totalmente independente dos outros processos do computador. E é ai que se encontra a maior diferença do docker para máquinas virtuais, máquinas virtuais não tem apenas o ambiente com as dependências da aplicação e sim todo um sistema operacional, o que ocupa muito mais espaço de armazenamento e se torna mais custoso.

Cada container enxerga e tem acesso apenas aquilo que diz respeito a aplicação e essa divisão é feita por meio de [[cgroups]] e [[namespaces]]

Um container necessita de uma parte da memória e dá CPU para funcionar pois será necessário algumas coisas da própria máquina onde a aplicação roda corretamente, então variáveis de precisam estar no container, interface de rede, etc, é realmente como se fosse o sistema operacional mas separado das outras aplicações.

Containers apenas continuam sendo executados se algum processo dentro dele ainda estiver em ativa. Caso contrário são fechados imediatamente.

