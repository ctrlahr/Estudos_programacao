## Map

A estrutura map é utilizada quando se precisa armazenar os dados eficientemente e através de uma chave resgatar os valores. É possível atribuir valores a algumas chaves específicas, por exemplo, em um array com a idade de várias pessoas para conseguir a idade de alguém em específico, seria necessário precorrer todo o array já em um map somente é necessário passar a chave. 
O map é basicamente o dicionário da maioria das linguagens.

Anteriormente existia a estrutura dictionary mas ela foi substituída pelo map.

#### Principais métodos Map
`put()` - Adiciona um par chave-valor

`putall()` - Adiciona todos os pares de outro map

`get()` - Retorna valor da chave ou null se não existir

`remove()` - remove o par pela chave

`size()` - Retorna a quantidade de números de pares chave-valor, ou seja, a quantidade de elementos



Map é uma interface, então não é possível instanciar ela diretamente, é necessário utilizar uma das classes sólidas entre HashMap, LinkedHashMap e TreeMap.

## HashMap
O hashmap é o mais rápido entre os três geralmente conseguindo Operações O(1) porém não mantem nenhum tipo de ordem, seja alfabética, numérica ou de inserção.
Algo interessante é que hashmaps podem ter uma chave null mas apenas uma por que as chaves devem ser únicas já os valores podem ter vários null justamente por que eles não precisam ser únicos.

Para criar um hashmap é necessário informar o tipo de dado tanto da chave quanto do valor:
![[Pasted image 20251010100651.png]]

No geral hashmaps são principalmente utilizados quando se preza por velocidade e quando a ordem não importa.

## LinkedHashMap
Diferentemente do hashmap, as LinkedHashMaps mantem uma ordem sendo a ordem no qual os elementos foram inseridos porém, em contraponto elas são mais lentas que o hashmap.

Para criar uma LinkedHashMap é assim:
![[Pasted image 20251010103057.png]]

No geral LinkedHashMap são principalmente utilizadas quando se prioriza ordem sobre performance.


## TreeMap
A estrutura TreeMap pode ordenar de forma natural por inserção assim como o LinkedHashMap mas também consegue realizar ordenações específicas como alfabética, decrescente, crescente, etc. Isso por meio de um comparator.
Ele também é bem mais lento que as outras duas estruturas, tendo geralmente operações O(log n)

Para criar um TreeMap basta fazer isso:
![[Pasted image 20251010103541.png]]

No geral TreeMaps são utilizados quando se preza por uma ordem específica como alfabética e quando não se precisa de tanto desempenho e performance.