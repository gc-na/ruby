<!--
Meta Description: # O Verdadeiro em Ruby: Compreendendo o `true` ## Sinopse No Ruby, `true` é um valor booleano que representa a verdade. É um dos dois valores lógicos ...
Meta Keywords: true, ruby, que, false, uso
-->

# O Verdadeiro em Ruby: Compreendendo o `true`

## Sinopse
No Ruby, `true` é um valor booleano que representa a verdade. É um dos dois valores lógicos primários, sendo o outro `false`. Este artigo explora o uso e a importância de `true` na programação Ruby.

## Documentação
### Propósito
O valor `true` é fundamental em lógica de controle e decisões dentro do código Ruby. Ele é utilizado para avaliar expressões booleanas em estruturas condicionais, como `if`, `unless`, e em loops.

### Uso
No Ruby, `true` é utilizado da seguinte forma:

```ruby
if true
  puts "Isso é verdade!"
end
```

Além disso, `true` pode ser utilizado em métodos que retornam valores booleanos, permitindo que os desenvolvedores verifiquem condições em tempo de execução.

### Detalhes
- **Tipo**: `true` é um objeto da classe `TrueClass`.
- **Comparação**: O valor `true` é considerado verdadeiro em todas as avaliações booleanas, exceto quando comparado diretamente com `false` ou `nil`.
- **Booleanos em Ruby**: Em Ruby, todos os objetos são verdadeiros, exceto `false` e `nil`.

## Exemplos
### Exemplo Básico
```ruby
# Exemplo de uso do true em uma condição
if true
  puts "Essa condição é verdadeira!"
end
```

### Uso em Métodos
```ruby
def verifica_par(num)
  num % 2 == 0
end

puts verifica_par(4) # Saída: true
```

### Iteração com Condição
```ruby
(1..5).each do |num|
  puts "#{num} é par?" if verifica_par(num)
end
```

## Explicação
Um erro comum ao trabalhar com `true` é confundir seu uso em expressões booleanas. Por exemplo, o uso de `if true == false` resultará em um erro lógico, pois essa expressão é sempre falsa. Além disso, é importante lembrar que em Ruby apenas `false` e `nil` são considerados falsos; todos os outros valores, incluindo `true`, são considerados verdadeiros.

### Armadilhas Comuns
- **Comparação Direta**: Evite comparar diretamente `true` com outros valores sem necessidade, pois isso pode gerar confusão. Use `if condition` em vez de `if condition == true`.
- **Confusão com Nil**: Lembre-se de que `nil` não é o mesmo que `false`, e ambos são considerados falsos, o que pode levar a erros se não forem tratados adequadamente.

## Resumo em Uma Frase
`true` é um valor booleano em Ruby que representa a verdade e é utilizado para controlar a lógica em estruturas condicionais e loops.