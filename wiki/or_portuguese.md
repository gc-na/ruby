<!--
Meta Description: # O Operador "or" em Ruby: Entenda Seu Funcionamento ## Sinopse O operador "or" em Ruby é uma ferramenta fundamental para controle de fluxo, permitind...
Meta Keywords: operador, ruby, para, uma, que
-->

# O Operador "or" em Ruby: Entenda Seu Funcionamento

## Sinopse
O operador "or" em Ruby é uma ferramenta fundamental para controle de fluxo, permitindo a combinação de expressões booleanas e facilitando a tomada de decisões em seu código.

## Documentação
O operador "or" é um operador lógico em Ruby que avalia duas expressões booleanas, retornando `true` se pelo menos uma delas for verdadeira. Ele é frequentemente utilizado em estruturas de controle, como condicionais e loops, para definir comportamentos alternativos.

### Propósito
O principal propósito do operador "or" é permitir que os desenvolvedores criem condições que podem ser verdadeiras com base em múltiplos critérios. Ele é especialmente útil em situações onde se deseja executar um bloco de código se uma ou mais condições forem satisfeitas.

### Uso
O operador "or" pode ser utilizado de várias maneiras:
1. Em condicionais para executar códigos com base na veracidade de uma ou mais condições.
2. Para definir valores padrão, onde um valor é usado se outro for `nil` ou `false`.

### Detalhes
- O operador "or" tem uma precedência menor do que outros operadores lógicos, como "&&" (e lógico). Portanto, ao usá-lo em expressões complexas, pode ser necessário usar parênteses para garantir que as operações sejam realizadas na ordem correta.

## Exemplos
### Exemplo 1: Uso básico do "or"
```ruby
x = nil
y = 10

resultado = x || y # resultado será 10
puts resultado
```

### Exemplo 2: Condicional com "or"
```ruby
idade = 15

if idade < 18 or idade > 65
  puts "Você é elegível para descontos."
else
  puts "Você não é elegível para descontos."
end
```

### Exemplo 3: Definindo valores padrão
```ruby
nome = nil
nome_padrao = "Usuário Desconhecido"

nome_final = nome or nome_padrao # nome_final será "Usuário Desconhecido"
puts nome_final
```

## Explicação
Um ponto importante a ser observado ao usar o operador "or" é sua precedência. Por exemplo, considere a expressão:

```ruby
resultado = true or false
```
Nesse caso, `resultado` será `true`, pois a expressão `or` não altera o valor de `resultado`, que é avaliado antes do operador. Para evitar confusões, recomenda-se usar parênteses:

```ruby
resultado = (true or false) # resultado será true
```

Outra armadilha comum é confundir "or" com "||". Enquanto ambos são operadores lógicos, "||" tem uma precedência maior, o que pode levar a resultados inesperados se não forem utilizados corretamente.

## Resumo em Uma Linha
O operador "or" em Ruby é um operador lógico que retorna `true` se pelo menos uma das expressões booleanas for verdadeira, sendo útil para controle de fluxo e definição de valores padrão.