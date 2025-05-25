<!--
Meta Description: # Comando "break" em Ruby: Entenda Como Utilizá-lo ## Sinopse O comando `break` em Ruby é utilizado para interromper a execução de um bloco de código,...
Meta Keywords: break, ruby, para, que, uma
-->

# Comando "break" em Ruby: Entenda Como Utilizá-lo

## Sinopse
O comando `break` em Ruby é utilizado para interromper a execução de um bloco de código, como loops e iteradores, permitindo que o controle seja transferido para o próximo nível de execução.

## Documentação
O `break` é uma palavra-chave fundamental em Ruby que serve para sair de loops, como `while`, `until`, `for`, e métodos iteradores como `each`. Quando executado, o `break` encerra a iteração atual e retorna o controle para o ponto imediatamente após o bloco que contém o loop.

### Propósito
O principal propósito do `break` é proporcionar uma maneira de sair de uma estrutura de repetição quando uma condição específica é atendida, evitando a execução desnecessária de iterações adicionais.

### Uso
A sintaxe básica do `break` é simplesmente a palavra-chave `break` dentro de um loop. É possível também passar um valor para o `break`, que será retornado como resultado do loop.

**Exemplo de sintaxe:**
```ruby
loop do
  # código
  break if condição
end
```

## Exemplos

### Exemplo 1: Uso Básico com `while`
```ruby
contador = 0
while contador < 5
  puts contador
  contador += 1
  break if contador == 3
end
# Saída: 0, 1, 2
```

### Exemplo 2: Uso com `each`
```ruby
números = [1, 2, 3, 4, 5]
números.each do |n|
  break if n == 4
  puts n
end
# Saída: 1, 2, 3
```

### Exemplo 3: Retornando um valor com `break`
```ruby
soma = 0
(1..10).each do |n|
  break soma if n > 5
  soma += n
end
puts soma
# Saída: 15 (1 + 2 + 3 + 4 + 5)
```

## Explicação
Embora o `break` seja uma ferramenta poderosa, existem algumas armadilhas comuns a serem observadas:

- **Escopo do `break`:** O `break` só afeta o loop mais interno. Se houver loops aninhados, o `break` só interrompe o loop em que está diretamente contido.
- **Uso em métodos:** O valor retornado pelo `break` pode ser utilizado, mas deve-se ter cuidado com o escopo e o contexto em que o `break` é chamado.
- **Iteradores personalizados:** Ao criar seus próprios iteradores, o comportamento do `break` pode não ser o esperado, a menos que você implemente explicitamente um mecanismo para lidar com ele.

## Resumo em Uma Linha
O comando `break` em Ruby permite interromper loops e iteradores, transferindo o controle para o ponto imediatamente após a estrutura de repetição.