## ==
O == é utilizado quando precisamos comparar se um valor é igual a outro em questão de igualdade mesmo então por exemplo:
```
let a = 10
let b = 10
let x = a == b // Vai estar retornando true
```

## ===
No javascript usamos o === quando queremos fazer uma comparação de tipos então por exemplo se quisermos saber se uma variavel de valor '10' é igual a outra de valor 10 nós utilizamos o === assim:
```
let a = '10'
let b = 10
let x = a === b // Vai estar retornando false
```

## object.is()
O método **`Object.is()`** determina se dois valores correspondem ao mesmo valor também:
`Object.is(value1, value2)`


Isso _não é_ o mesmo que ser igual de acordo com o operador `==` O operador `==` aplica diversas coerções para ambos os lados (se eles não correspondem ao mesmo Tipo) antes de testar a igualdade (resultando em comportamentos como a comparação `"" == false` retornar `true`), enquanto `Object.is` não realiza a coerção de nenhum dos valores.

Isso também _não_ _é_ o mesmo que ser igual de acordo com o operador `===`. O operador `===` (assim como o operador `==` trata os valores numéricos `-0` e `+0` como iguais e trata `Number.NaN` como não igual a `NaN`.
