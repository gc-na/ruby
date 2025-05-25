<!--
Meta Description: # Strings em Ruby: Tudo o que Você Precisa Saber ## Sinopse Strings em Ruby são sequências de caracteres utilizadas para armazenar e manipular texto. ...
Meta Keywords: strings, ruby, que, string, uma
-->

# Strings em Ruby: Tudo o que Você Precisa Saber

## Sinopse
Strings em Ruby são sequências de caracteres utilizadas para armazenar e manipular texto. Elas são objetos da classe `String`, oferecendo uma variedade de métodos para facilitar operações comuns de manipulação de texto.

## Documentação
As strings em Ruby são representadas pela classe `String`, que fornece uma interface rica para trabalhar com texto. Você pode criar uma string de várias maneiras, sendo as mais comuns a utilização de aspas simples (`'`) e aspas duplas (`"`). As strings em Ruby são imutáveis, o que significa que qualquer operação que modifique uma string retornará uma nova string em vez de alterar a original.

### Propósito
O objetivo das strings em Ruby é permitir que os desenvolvedores manipulem texto de forma eficiente, realizando operações como concatenação, substituição, formatação e busca.

### Uso
Para criar uma string, você pode usar:
```ruby
str1 = 'Olá, mundo!'
str2 = "Ruby é incrível!"
```

Além disso, Ruby oferece métodos como `length`, `upcase`, `downcase`, `strip`, `gsub`, entre outros, para manipulação de strings.

### Detalhes
- **Aspas Simples vs. Aspas Duplas**: Strings entre aspas simples não interpretam caracteres de escape (exceto para `\\` e `\'`), enquanto strings entre aspas duplas sim.
- **Imutabilidade**: Strings em Ruby são imutáveis, então métodos como `gsub` retornam uma nova string ao invés de modificar a original.
- **Interpolação de Strings**: Com aspas duplas, você pode inserir valores de variáveis diretamente na string usando `#{}`.

## Exemplos
```ruby
# Criando strings
greeting = "Olá"
name = "Maria"

# Concatenando strings
message = greeting + ", " + name + "!"
puts message  # Saída: Olá, Maria!

# Usando métodos de string
puts message.length  # Saída: 15
puts message.upcase   # Saída: OLÁ, MARIA!

# Interpolação
age = 30
puts "#{name} tem #{age} anos."  # Saída: Maria tem 30 anos.
```

## Explicação
Um dos erros comuns ao trabalhar com strings em Ruby é a confusão entre aspas simples e duplas. Lembre-se de que apenas strings em aspas duplas permitem a interpolação de variáveis e a interpretação de caracteres especiais. Além disso, é importante ter em mente que, como strings são imutáveis, qualquer modificação resulta em uma nova string, o que pode levar a um consumo de memória maior se não for gerenciado corretamente.

## Resumo em Uma Linha
Strings em Ruby são objetos imutáveis que permitem a manipulação eficiente de texto através de uma ampla gama de métodos.