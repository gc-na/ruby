<!--
Meta Description: # Quando Usar o Método "when" em Ruby: Um Guia Completo ## Sinopse O método `when` em Ruby é usado dentro de uma estrutura de controle `case`, permiti...
Meta Keywords: when, ruby, case, que, puts
-->

# Quando Usar o Método "when" em Ruby: Um Guia Completo

## Sinopse
O método `when` em Ruby é usado dentro de uma estrutura de controle `case`, permitindo uma forma clara e concisa de realizar comparações de múltiplas condições.

## Documentação
O `when` é um componente fundamental na construção de instruções condicionais em Ruby. Ele permite que você verifique um valor contra várias condições possíveis. O uso do `case` combinado com `when` torna o código mais legível e organizado em comparação com várias instruções `if`.

### Propósito
O propósito do `when` é simplificar a lógica de comparação, tornando o código mais fácil de entender e manter.

### Uso
A estrutura básica de um `case` com `when` é a seguinte:

```ruby
case valor_a_comparar
when condição1
  # Código a ser executado se condição1 for verdadeira
when condição2
  # Código a ser executado se condição2 for verdadeira
else
  # Código a ser executado se nenhuma condição for verdadeira
end
```

## Exemplos

### Exemplo 1: Uso Simples do `when`
```ruby
dia_da_semana = 'sexta'

case dia_da_semana
when 'segunda'
  puts 'Hoje é segunda-feira.'
when 'sexta'
  puts 'Hoje é sexta-feira.'
else
  puts 'É outro dia da semana.'
end
```
**Saída:** Hoje é sexta-feira.

### Exemplo 2: Comparação de Números
```ruby
nota = 85

case nota
when 90..100
  puts 'Excelente'
when 80..89
  puts 'Bom'
when 70..79
  puts 'Satisfatório'
else
  puts 'Precisa melhorar'
end
```
**Saída:** Bom.

## Explicação
Um dos erros comuns ao usar `when` é esquecer de incluir a cláusula `else`, o que pode levar a situações em que nenhuma condição é atendida e nada é executado. Além disso, é importante lembrar que você pode usar intervalos (como `90..100`) e expressões booleanas nas condições.

Outro ponto a considerar é que as condições no `when` são avaliadas na ordem em que aparecem. Portanto, mais condições específicas devem ser listadas antes das mais gerais para evitar que um valor correspondente seja capturado pela condição errada.

## Resumo em Uma Linha
O método `when` em Ruby permite realizar comparações de múltiplas condições de forma clara e eficiente dentro de uma estrutura `case`.