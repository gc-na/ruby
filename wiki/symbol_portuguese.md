<!--
Meta Description: # Símbolo em Ruby: Entenda o seu Uso e Aplicações ## Sinopse Os símbolos em Ruby são objetos imutáveis que representam nomes e strings de forma eficie...
Meta Keywords: símbolos, ruby, são, que, símbolo
-->

# Símbolo em Ruby: Entenda o seu Uso e Aplicações

## Sinopse
Os símbolos em Ruby são objetos imutáveis que representam nomes e strings de forma eficiente, sendo amplamente utilizados como identificadores e chaves em hashes.

## Documentação
### O que é um Símbolo?
Um símbolo em Ruby é um tipo de objeto que, ao contrário das strings, é imutável e único na memória. Eles são definidos precedendo um nome com dois pontos (`:`), como `:meu_simbolo`. Os símbolos são frequentemente usados para representar identificadores, nomes de métodos e chaves em hashes, oferecendo vantagens em termos de desempenho e consumo de memória.

### Propósito
Os símbolos são utilizados quando você precisa de um identificador que não será alterado. Por serem imutáveis, a criação de um símbolo é mais eficiente do que a criação de uma string, especialmente quando a mesma sequência de caracteres é utilizada repetidamente.

### Uso
Para criar um símbolo, basta preceder o nome com dois pontos. Por exemplo:
```ruby
meu_simbolo = :exemplo
```
Os símbolos podem ser usados como chaves em hashes:
```ruby
hash = { nome: "João", idade: 30 }
```
Aqui, `:nome` e `:idade` são símbolos que atuam como chaves.

## Exemplos
### Exemplo 1: Criação e uso básico
```ruby
# Criando um símbolo
simbolo = :teste

# Imprimindo o símbolo
puts simbolo  # Saída: teste
```

### Exemplo 2: Símbolos em um hash
```ruby
# Usando símbolos como chaves em um hash
pessoa = { nome: "Maria", idade: 25, cidade: "São Paulo" }

# Acessando valores através de símbolos
puts pessoa[:nome]  # Saída: Maria
```

### Exemplo 3: Comparação entre String e Símbolo
```ruby
# Comparando desempenho
string = "exemplo"
simbolo = :exemplo

puts string.object_id == simbolo.object_id  # Saída: false
```
Os símbolos são sempre únicos, mesmo que criados várias vezes.

## Explicação
### Armadilhas Comuns
- **Imutabilidade**: Os símbolos não podem ser alterados após sua criação, o que pode ser confuso para iniciantes. Diferentemente das strings, que podem ser modificadas, os símbolos são fixos.
- **Consumo de Memória**: Embora os símbolos sejam mais eficientes em termos de memória, se você criar muitos símbolos dinâmicos (por exemplo, a partir de entrada do usuário), pode acabar consumindo toda a memória do Ruby, pois os símbolos não são coletados pelo Garbage Collector.
- **Cuidado com a Comparação**: Sempre use símbolos quando precisar de um identificador constante. Usar strings pode levar a comportamentos inesperados em comparações.

## Resumo em Uma Linha
Símbolos em Ruby são objetos imutáveis eficientes, utilizados como identificadores e chaves em hashes, proporcionando melhor desempenho em comparação a strings.