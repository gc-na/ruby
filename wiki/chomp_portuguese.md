<!--
Meta Description: # Chomp em Ruby: Entenda como remover quebras de linha ## Sinopse O método `chomp` em Ruby é utilizado para remover caracteres de nova linha (como `\n...
Meta Keywords: chomp, string, linha, ruby, uma
-->

# Chomp em Ruby: Entenda como remover quebras de linha

## Sinopse
O método `chomp` em Ruby é utilizado para remover caracteres de nova linha (como `\n` ou `\r\n`) do final de uma string, facilitando o tratamento de entradas de texto.

## Documentação
O método `chomp` é uma função de string que serve para eliminar caracteres de quebra de linha. Ele é frequentemente usado ao lidar com entradas de usuário ou ao ler arquivos de texto, onde quebras de linha são comuns.

### Propósito
O propósito do `chomp` é simplificar o processamento de strings, permitindo que desenvolvedores retirem quebras de linha indesejadas que podem causar problemas em manipulações de string ou comparações.

### Uso
A sintaxe básica do `chomp` é a seguinte:

```ruby
string.chomp([separator])
```

- `string`: A string da qual se deseja remover os caracteres de final.
- `separator`: Um caractere ou sequência de caracteres opcional que se deseja remover. Se não for especificado, o padrão é a quebra de linha.

### Detalhes
- O método `chomp` não altera a string original; em vez disso, ele retorna uma nova string.
- Se a string não terminar com o caractere especificado ou com uma quebra de linha, ela permanece inalterada.

## Exemplos

### Exemplo 1: Uso Básico do Chomp

```ruby
texto = "Olá, mundo!\n"
resultado = texto.chomp
puts resultado  # Saída: "Olá, mundo!"
```

### Exemplo 2: Removendo um Separador Específico

```ruby
texto = "data.csv\r\n"
resultado = texto.chomp(".csv")
puts resultado  # Saída: "data"
```

### Exemplo 3: Chomp em Entrada do Usuário

```ruby
print "Digite seu nome: "
nome = gets.chomp
puts "Olá, #{nome}!"  # Remove a quebra de linha após a entrada do usuário
```

## Explicação
Um erro comum ao usar `chomp` é esquecer que ele não altera a string original. Se você precisa da string sem a quebra de linha, deve armazenar o resultado em uma nova variável ou sobrescrever a variável original. Outro ponto importante é que, se um separador específico for passado, ele só será removido se estiver exatamente no final da string. Caso contrário, a string permanecerá inalterada.

## Resumo em Uma Linha
O método `chomp` em Ruby remove quebras de linha do final de uma string, facilitando o tratamento de entradas de texto.