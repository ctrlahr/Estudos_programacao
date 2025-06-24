## Inteiros signed
O tipo signed é aquele que suporta valores negativos e positivos, esses tipos signed podem ter tamanho de 8 bits, 16, 32, 64, 128 ou isize(cujo tamanho depende da arquitetura do sistema em que o programa está sendo executado, ou seja, se o programa for executado em uma máquina de 32bits ele terá tamanho de 32bits já se for executado em uma de 64 ele terá esse tamanho). Nos tipos signed um bit é reservado para o sinal do nosso número fazendo com que dessa forma casas a mais sejam ocupadas.

O intervalo dos valores signed são de -128 até 127 sendo a formula para calcularmos isso:
$$
-(2ⁿ¯¹) 
$$
Dessa fórmula até essa
$$ 2ⁿ¯¹ - 1$$

## Inteiros unsigned
Os tipos unsigned suportam apenas valores não negativos, ou seja, de zero para cima. Os unsigned de forma igual aos signed podem ocupar 8, 16, 32, 64, 128 ou usize bits sendo usize a mesma coisa do isize.

O intervalo dos valores unsigned são de 0 até 255 sendo a fórmula para calcularmos isso:
$$
2ⁿ - 1
$$
- De 0 até o resultado dessa fórmula

| Bits | Signed | Unsigned |
| ---- | ------ | -------- |
| 8    | i8     | u8       |
| 16   | i16    | u16      |
| 32   | i32    | u32      |
| 64   | i64    | u64      |
| 128  | i128   | u128     |
| arch | isize  | usize    |

Quando não especificamos qual o tipo que vamos utilizar por padrão o rust escolhe o `i32`