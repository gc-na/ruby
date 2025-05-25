<!--
Meta Description: # Definição de Métodos em Ruby: Compreendendo o 'def' ## Sinopse O comando `def` em Ruby é utilizado para definir métodos, permitindo que os desenvolv...
Meta Keywords: ruby, def, métodos, método, parâmetros
-->

# Definição de Métodos em Ruby: Compreendendo o 'def'

## Sinopse
O comando `def` em Ruby é utilizado para definir métodos, permitindo que os desenvolvedores encapsulem lógica reutilizável em uma estrutura organizada e compreensível.

## Documentação
O `def` é uma palavra-chave essencial na linguagem Ruby que serve para declarar métodos. Métodos são blocos de código que realizam uma tarefa específica e podem ser chamados em diferentes partes do programa. A definição de um método começa com a palavra-chave `def`, seguida pelo nome do método e, opcionalmente, uma lista de parâmetros.

### Sintaxe
```ruby
def nome_do_metodo(param1, param2)
  # corpo do método
end
```

### Propósito
O objetivo principal do `def` é ajudar na organização do código, promovendo a reutilização e a legibilidade. Ao encapsular funcionalidades em métodos, o código se torna mais fácil de entender e manter.

### Uso
- **Definindo um método sem parâmetros**
```ruby
def saudacao
  puts "Olá, mundo!"
end
```

- **Definindo um método com parâmetros**
```ruby
def soma(a, b)
  a + b
end
```

- **Chamando um método**
```ruby
saudacao          # Saída: Olá, mundo!
resultado = soma(5, 3)  # resultado agora é 8
```

## Exemplos
1. **Método sem parâmetros**
```ruby
def mensagem
  "Aprendendo Ruby!"
end

puts mensagem  # Saída: Aprendendo Ruby!
```

2. **Método com parâmetros**
```ruby
def multiplicar(x, y)
  x * y
end

puts multiplicar(4, 5)  # Saída: 20
```

3. **Método com valor de retorno**
```ruby
def divisao(x, y)
  return "Divisão por zero" if y == 0
  x / y
end

puts divisao(10, 2)  # Saída: 5
puts divisao(10, 0)  # Saída: Divisão por zero
```

## Explicação
### Armadilhas Comuns
- **Nomes de Métodos**: Os nomes dos métodos devem ser descritivos e seguir a convenção de nomenclatura em snake_case. Evite nomes genéricos que não indiquem a ação realizada.
- **Parâmetros Opcionais**: Ruby permite parâmetros opcionais, mas é importante lembrar que isso pode complicar a lógica se não for bem documentado.
- **Escopo**: Métodos definidos dentro de classes têm um escopo diferente de métodos definidos em módulos ou globalmente. Isso pode levar a confusões sobre onde um método pode ser chamado.

### Observações Adicionais
- Métodos podem ser definidos como públicos, privados ou protegidos, controlando o acesso a eles.
- O uso de `return` é opcional em Ruby; o valor da última linha do método é retornado automaticamente.

## Resumo em Uma Linha
O `def` em Ruby é utilizado para definir métodos, permitindo a criação de código organizado e reutilizável.