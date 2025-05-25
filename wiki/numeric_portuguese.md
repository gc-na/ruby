<!--
Meta Description: # Numeric em Ruby: O Guia Completo ## Sinopse O módulo `Numeric` em Ruby é a superclasse para todos os tipos de números no Ruby, incluindo inteiros e ...
Meta Keywords: ruby, numeric, números, métodos, operações
-->

# Numeric em Ruby: O Guia Completo

## Sinopse
O módulo `Numeric` em Ruby é a superclasse para todos os tipos de números no Ruby, incluindo inteiros e números de ponto flutuante. Ele fornece uma interface comum e métodos que permitem a manipulação e operações aritméticas sobre números.

## Documentação
O módulo `Numeric` é uma parte fundamental da linguagem Ruby, servindo como um ponto de partida para vários tipos de dados numéricos. Ele herda de `Object` e é estendido por classes como `Integer`, `Float` e `Complex`. O `Numeric` é responsável por métodos que possibilitam realizar operações matemáticas e comparações.

### Propósito
O propósito do módulo `Numeric` é fornecer métodos que simplificam operações aritméticas e comparações entre números. Ele define funções que podem ser utilizadas por todos os números, independentemente de suas representações específicas.

### Uso
Para utilizar os métodos do `Numeric`, você pode instanciar classes que o herdam, como `Integer` ou `Float`. A maioria dos métodos pode ser chamada diretamente em instâncias de números.

### Detalhes
Os principais métodos disponíveis no módulo `Numeric` incluem:
- `+`, `-`, `*`, `/` - Operações aritméticas básicas.
- `**` - Exponenciação.
- `abs` - Retorna o valor absoluto do número.
- `ceil`, `floor`, `round` - Métodos de arredondamento.
- `to_f`, `to_i` - Conversão entre diferentes tipos numéricos.

## Exemplos

### Exemplo 1: Operações Aritméticas
```ruby
a = 10
b = 3.5

soma = a + b      # => 13.5
subtracao = a - b # => 6.5
multiplicacao = a * b # => 35.0
divisao = a / b   # => 2.857142857142857
```

### Exemplo 2: Métodos de Conversão
```ruby
num = 5.7

inteiro = num.to_i  # => 5
flutuante = num.to_f # => 5.7
```

### Exemplo 3: Valor Absoluto
```ruby
valor_negativo = -42
valor_absoluto = valor_negativo.abs  # => 42
```

### Exemplo 4: Arredondamento
```ruby
numero = 3.6

arredondado_cima = numero.ceil   # => 4
arredondado_baixo = numero.floor  # => 3
arredondado = numero.round         # => 4
```

## Explicação
Um dos principais cuidados ao trabalhar com o módulo `Numeric` é entender como Ruby trata a divisão entre inteiros. Por exemplo, a divisão de dois inteiros sempre resulta em um número de ponto flutuante, a menos que se utilize a divisão inteira (`div` ou `//`). Além disso, a precisão dos números de ponto flutuante pode levar a resultados inesperados em operações complexas devido a como esses números são representados na memória.

## Resumo em Uma Linha
O módulo `Numeric` em Ruby fornece uma interface comum e métodos para manipulação de todos os tipos de números, facilitando operações aritméticas e conversões.