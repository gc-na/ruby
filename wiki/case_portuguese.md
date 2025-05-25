<!--
Meta Description: # Estrutura de Controle `case` no Ruby: Entenda Como Utilizá-la com Eficiência ## Sinopse A estrutura de controle `case` em Ruby permite a execução co...
Meta Keywords: case, when, uma, puts, ruby
-->

# Estrutura de Controle `case` no Ruby: Entenda Como Utilizá-la com Eficiência

## Sinopse
A estrutura de controle `case` em Ruby permite a execução condicional de diferentes blocos de código com base no valor de uma expressão, proporcionando uma maneira limpa e legível de lidar com múltiplas condições.

## Documentação
A estrutura `case` é uma maneira poderosa e intuitiva de implementar lógica condicional em Ruby. Ela é semelhante à instrução `switch` encontrada em outras linguagens de programação, mas com uma sintaxe mais elegante e flexível.

### Propósito
O `case` é utilizado para avaliar uma expressão e executar um bloco de código correspondente ao valor dessa expressão. Isso torna a leitura e a manutenção do código mais fáceis, especialmente quando há várias condições a serem testadas.

### Sintaxe Básica
A sintaxe do `case` em Ruby é a seguinte:

```ruby
case expressão
when valor1
  # código a ser executado se expressão == valor1
when valor2
  # código a ser executado se expressão == valor2
else
  # código a ser executado se nenhum valor corresponder
end
```

## Exemplos

### Exemplo 1: Uso Básico do `case`
```ruby
dia = "domingo"

case dia
when "segunda-feira"
  puts "Hoje é dia de trabalho!"
when "domingo"
  puts "Hoje é dia de descanso!"
else
  puts "Dia não especificado."
end
```
**Saída:** Hoje é dia de descanso!

### Exemplo 2: Usando `case` com Intervalos
```ruby
nota = 85

case nota
when 90..100
  puts "Nota A"
when 80..89
  puts "Nota B"
when 70..79
  puts "Nota C"
else
  puts "Nota abaixo do esperado"
end
```
**Saída:** Nota B

### Exemplo 3: Usando `case` com Expressões
```ruby
numero = 15

case
when numero < 10
  puts "Número é menor que 10"
when numero < 20
  puts "Número está entre 10 e 20"
else
  puts "Número é 20 ou maior"
end
```
**Saída:** Número está entre 10 e 20

## Explicação
- **Comparação de Tipos:** O `case` utiliza a comparação `===`, o que significa que pode haver diferenças em como ele lida com diferentes tipos de valores. Isso é especialmente relevante quando se utiliza intervalos ou expressões regulares.
- **Cuidado com o `else`:** A cláusula `else` é opcional, mas é uma boa prática incluí-la para lidar com casos em que nenhum dos `when` é satisfeito.
- **Uso de `case` sem uma expressão:** É possível usar `case` sem especificar uma expressão, permitindo que cada cláusula `when` avalie uma condição. Este recurso pode ser útil para simplificar certas lógicas.

## Resumo em Uma Linha
A estrutura de controle `case` em Ruby permite a execução condicional de blocos de código de forma clara e legível, facilitando a lógica de múltiplas condições.