<!--
Meta Description: # Estrutura Condicional "if" no Ruby: Compreenda e Domine ## Sinopse A estrutura condicional "if" é uma das principais ferramentas de controle de flux...
Meta Keywords: ruby, código, puts, condições, para
-->

# Estrutura Condicional "if" no Ruby: Compreenda e Domine

## Sinopse
A estrutura condicional "if" é uma das principais ferramentas de controle de fluxo na linguagem Ruby, permitindo que o programador execute blocos de código com base em condições específicas.

## Documentação
A estrutura "if" em Ruby é utilizada para executar um bloco de código se uma determinada condição for verdadeira. Se a condição for falsa, o Ruby ignora o bloco. A sintaxe básica da estrutura "if" é a seguinte:

```ruby
if condição
  # código a ser executado se a condição for verdadeira
end
```

### Uso
A condição pode ser qualquer expressão que retorne um valor booleano (`true` ou `false`). O bloco de código associado ao "if" será executado somente quando a condição for avaliada como verdadeira.

#### Sintaxe Alternativa
Ruby também permite o uso de "elsif" e "else" para maior controle de fluxo:

```ruby
if condição1
  # código se condição1 for verdadeira
elsif condição2
  # código se condição2 for verdadeira
else
  # código se nenhuma das condições anteriores forem verdadeiras
end
```

## Exemplos
### Exemplo Básico
```ruby
idade = 18

if idade >= 18
  puts "Você é maior de idade."
end
```

### Usando "elsif" e "else"
```ruby
nota = 75

if nota >= 90
  puts "Conceito A"
elsif nota >= 75
  puts "Conceito B"
elsif nota >= 60
  puts "Conceito C"
else
  puts "Reprovado"
end
```

### Condições Múltiplas
```ruby
temperatura = 30

if temperatura > 30
  puts "Está quente."
elsif temperatura < 15
  puts "Está frio."
else
  puts "A temperatura está agradável."
end
```

## Explicação
### Armadilhas Comuns
- **Uso de `=` ao invés de `==`**: Lembre-se de que `=` é um operador de atribuição, enquanto `==` é usado para comparação. Usar `=` em um "if" resultará em um erro ou em um comportamento inesperado.
  
- **Avaliação de condições**: Em Ruby, qualquer valor diferente de `nil` ou `false` é considerado verdadeiro. Isso pode levar a confusões se não for bem entendido.

- **Indentação**: Embora Ruby não exija indentação para a execução do código, uma boa prática de indentar facilita a leitura e manutenção do código.

### Notas Adicionais
- O Ruby também permite o uso da sintaxe de uma linha para condições simples, utilizando o operador ternário, o que pode ser útil para expressões simples:
  
```ruby
resultado = idade >= 18 ? "Maior de idade" : "Menor de idade"
```

## Resumo em Uma Linha
A estrutura condicional "if" no Ruby permite executar blocos de código com base na avaliação de condições lógicas.