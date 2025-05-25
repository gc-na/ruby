<!--
Meta Description: # O Comando "while" em Ruby: Estruturas de Repetição Eficientes ## Sinopse O comando "while" em Ruby é uma estrutura de controle que permite a execuçã...
Meta Keywords: while, condição, contador, que, bloco
-->

# O Comando "while" em Ruby: Estruturas de Repetição Eficientes

## Sinopse
O comando "while" em Ruby é uma estrutura de controle que permite a execução repetida de um bloco de código enquanto uma condição especificada for verdadeira. É amplamente utilizado para criar laços de repetição, facilitando a execução de tarefas repetitivas com base em condições dinâmicas.

## Documentação
### Propósito
O comando "while" é utilizado para executar um bloco de código repetidamente até que a condição definida retorne um valor falso. Essa estrutura é particularmente útil quando não se sabe previamente quantas iterações serão necessárias, permitindo que o código continue a ser executado enquanto a condição for verdadeira.

### Uso
A sintaxe básica do comando "while" é a seguinte:

```ruby
while condição
  # bloco de código a ser executado
end
```

- **condição**: uma expressão que é avaliada antes da execução do bloco. Se a condição for verdadeira (`true`), o bloco de código será executado. Se for falsa (`false`), a execução do laço é interrompida.
- O bloco de código pode conter qualquer conjunto de instruções Ruby.

### Detalhes
- O comando "while" é uma estrutura de repetição que pode ser aninhada, permitindo a criação de laços dentro de laços.
- Ao utilizar "while", é importante garantir que a condição eventualmente se torne falsa, caso contrário, um loop infinito será criado, levando a um travamento do programa.

## Exemplos
### Exemplo 1: Contagem Simples
```ruby
contador = 1
while contador <= 5
  puts "Contador: #{contador}"
  contador += 1
end
```
Saída:
```
Contador: 1
Contador: 2
Contador: 3
Contador: 4
Contador: 5
```

### Exemplo 2: Loop Infinito
```ruby
# Atenção: este exemplo criará um loop infinito
# while true
#   puts "Este loop nunca termina!"
# end
```
**Nota**: O código acima é comentado para evitar um loop infinito. Remova o comentário para executá-lo, mas esteja ciente das consequências.

## Explicação
- **Armadilhas Comuns**: Um erro comum ao usar o "while" é não modificar a condição dentro do bloco, o que pode levar a um loop infinito. Sempre verifique se a condição será eventualmente falsa.
- **Uso de `break`**: Em alguns casos, pode ser desejável interromper um loop antes que a condição se torne falsa. Para isso, pode-se utilizar a palavra-chave `break` para sair do loop imediatamente.

## Resumo em Uma Linha
O comando "while" em Ruby permite a execução repetida de um bloco de código enquanto uma condição especificada for verdadeira, facilitando a criação de laços de repetição dinâmicos.