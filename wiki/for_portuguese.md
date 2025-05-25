<!--
Meta Description: # O Comando "for" em Ruby: Iteração Simples e Eficiente ## Sinopse O comando `for` em Ruby é uma estrutura de controle que permite iterar sobre coleçõ...
Meta Keywords: ruby, que, iteração, sobre, item
-->

# O Comando "for" em Ruby: Iteração Simples e Eficiente

## Sinopse
O comando `for` em Ruby é uma estrutura de controle que permite iterar sobre coleções, como arrays e ranges, facilitando o processamento de elementos de maneira sequencial.

## Documentação
O `for` é um loop que itera sobre uma coleção de objetos. A sintaxe básica é `for item in coleção`, onde `item` representa o elemento atual da iteração e `coleção` é o array ou range que está sendo percorrido. O bloco de código que segue a declaração `for` será executado para cada item da coleção.

### Sintaxe
```ruby
for item in coleção
  # código a ser executado para cada item
end
```

### Propósito
O principal objetivo do comando `for` é simplificar a iteração sobre coleções, permitindo que os desenvolvedores escrevam código de forma mais legível e clara.

## Exemplos
### Exemplo 1: Iterando sobre um Array
```ruby
frutas = ["maçã", "banana", "laranja"]
for fruta in frutas
  puts fruta
end
```
**Saída:**
```
maçã
banana
laranja
```

### Exemplo 2: Iterando sobre um Range
```ruby
for i in 1..5
  puts "Número: #{i}"
end
```
**Saída:**
```
Número: 1
Número: 2
Número: 3
Número: 4
Número: 5
```

### Exemplo 3: Usando `break` e `next`
```ruby
for i in 1..10
  next if i.even?
  puts i
end
```
**Saída:**
```
1
3
5
7
9
```

## Explicação
Embora o comando `for` seja uma maneira intuitiva de iterar, é importante notar algumas considerações:

- **Escopo de Variáveis**: A variável utilizada para a iteração (`item` no exemplo) terá seu escopo definido fora do bloco `for`, o que pode levar a comportamentos inesperados se a variável for utilizada fora do loop.
  
- **Alternativas**: Em Ruby, existem outras formas de iteração, como `each`, que são frequentemente preferidas por oferecerem uma sintaxe mais idiomática e segura.

- **Performance**: Para coleções grandes, o uso de `each` ou métodos enumeráveis pode ser mais eficiente em termos de desempenho.

## Resumo em Uma Linha
O comando `for` em Ruby permite a iteração simples e clara sobre coleções, facilitando a execução de operações em cada elemento.