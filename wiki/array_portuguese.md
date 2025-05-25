<!--
Meta Description: # Arrays em Ruby: Guia Completo e Prático ## Sinopse No Ruby, um Array é uma coleção ordenada de elementos que pode conter diferentes tipos de dados. ...
Meta Keywords: ruby, array, elementos, que, arrays
-->

# Arrays em Ruby: Guia Completo e Prático

## Sinopse
No Ruby, um Array é uma coleção ordenada de elementos que pode conter diferentes tipos de dados. Essa estrutura é altamente flexível e permite a manipulação eficiente de listas e sequências.

## Documentação
Os Arrays em Ruby são uma das estruturas de dados mais utilizadas, permitindo armazenar e gerenciar múltiplos valores sob um único nome. Cada elemento de um Array tem uma posição, começando do índice 0. Os Arrays podem conter qualquer tipo de objeto, incluindo outros Arrays.

### Propósito
O principal propósito do Array é organizar dados de forma que possam ser facilmente acessados e manipulados. Eles suportam uma variedade de operações, como adição, remoção e iteração sobre os elementos.

### Uso
Para criar um Array, você pode usar colchetes (`[]`) ou a classe `Array` diretamente. Aqui estão algumas operações comuns:

- Criação de um Array:
  ```ruby
  meu_array = [1, 2, 3, 4]
  outro_array = Array.new
  ```

- Acesso a elementos:
  ```ruby
  primeiro_elemento = meu_array[0] # => 1
  ```

- Adição de elementos:
  ```ruby
  meu_array.push(5) # => [1, 2, 3, 4, 5]
  ```

- Remoção de elementos:
  ```ruby
  meu_array.pop # => 5
  ```

## Exemplos
### Criação de um Array
```ruby
frutas = ["maçã", "banana", "laranja"]
```

### Acesso a Elementos
```ruby
puts frutas[1] # Saída: banana
```

### Iteração sobre um Array
```ruby
frutas.each do |fruta|
  puts fruta
end
```

### Filtragem de Elementos
```ruby
numeros = [1, 2, 3, 4, 5]
pares = numeros.select { |num| num.even? } # => [2, 4]
```

### Transformação de Elementos
```ruby
nomes = ["ana", "bruno", "carla"]
nomes_capitalizados = nomes.map(&:capitalize) # => ["Ana", "Bruno", "Carla"]
```

## Explicação
Embora os Arrays em Ruby sejam poderosos e flexíveis, existem alguns pontos que podem causar confusão:

- **Índices Negativos**: Usar índices negativos permite acessar elementos a partir do final do Array. Por exemplo, `frutas[-1]` retorna o último elemento.
- **Mutabilidade**: Arrays são mutáveis, o que significa que você pode alterar, adicionar ou remover elementos depois que o Array é criado.
- **Mistura de Tipos**: Você pode misturar diferentes tipos de dados em um mesmo Array, mas isso pode levar a erros se não for bem gerenciado.

Além disso, é importante lembrar que alguns métodos, como `map`, retornam um novo Array, enquanto outros, como `push`, modificam o Array original.

## Resumo em Uma Linha
Os Arrays em Ruby são coleções ordenadas e mutáveis de elementos que permitem manipulação eficiente de dados.