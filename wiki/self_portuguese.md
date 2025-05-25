<!--
Meta Description: # O que é "self" em Ruby: Entendendo o Contexto de Classe e Instância ## Sinopse O `self` em Ruby é uma palavra-chave que representa a instância atual...
Meta Keywords: self, instância, classe, carro, modelo
-->

# O que é "self" em Ruby: Entendendo o Contexto de Classe e Instância

## Sinopse
O `self` em Ruby é uma palavra-chave que representa a instância atual do objeto, seja em um contexto de classe ou de instância, permitindo o acesso a métodos e variáveis de instância de forma clara e concisa.

## Documentação
O `self` é um conceito fundamental na linguagem Ruby, utilizado para referir-se ao objeto que está executando o código em um determinado contexto. Isso é especialmente útil em métodos de instância e de classe, onde é necessário distinguir entre o objeto atual e outras instâncias ou classes.

### Propósito
O principal propósito do `self` é fornecer um modo de referenciar o objeto atual, o que é crucial para o funcionamento adequado de métodos, variáveis e outros elementos da programação orientada a objetos.

### Uso
- **Métodos de Instância**: Dentro de um método de instância, `self` refere-se à instância do objeto que está chamando o método.
- **Métodos de Classe**: Dentro de um método de classe, `self` refere-se à classe em si.
- **Atributos e Variáveis**: `self` é utilizado para acessar e modificar atributos e variáveis de instância.

### Detalhes
- `self` pode ser utilizado em qualquer parte de um objeto, desde que o contexto esteja claro. 
- Em um contexto de classe, ao definir métodos de classe, `self` é utilizado para indicar que o método é associado à própria classe, não a uma instância dela.

## Exemplos
### Exemplo 1: Método de Instância
```ruby
class Carro
  attr_accessor :modelo
  
  def initialize(modelo)
    @modelo = modelo
  end
  
  def mostrar_modelo
    "O modelo do carro é: #{self.modelo}"
  end
end

carro = Carro.new("Fusca")
puts carro.mostrar_modelo # => O modelo do carro é: Fusca
```

### Exemplo 2: Método de Classe
```ruby
class Carro
  def self.numero_de_rodas
    4
  end
end

puts Carro.numero_de_rodas # => 4
```

### Exemplo 3: Modificando Atributos
```ruby
class Carro
  attr_accessor :modelo
  
  def initialize(modelo)
    @modelo = modelo
  end

  def mudar_modelo(novo_modelo)
    self.modelo = novo_modelo
  end
end

carro = Carro.new("Fusca")
carro.mudar_modelo("Civic")
puts carro.modelo # => Civic
```

## Explicação
Um erro comum ao usar `self` é confundi-lo com a instância do objeto. É importante lembrar que `self` sempre se refere ao objeto que está executando o código no momento, o que pode mudar dependendo do contexto. Outro ponto a se observar é que, ao usar `self` para definir métodos de classe, você deve garantir que está chamando o método corretamente, pois métodos de instância não têm acesso a métodos de classe diretamente.

## Resumo em Uma Linha
O `self` em Ruby é uma referência ao objeto atual, essencial para acessar métodos e atributos em contextos de instância e de classe.