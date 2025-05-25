<!--
Meta Description: # Hash em Ruby: Estruturas de Dados Poderosas e Flexíveis ## Sinopse Os Hashes em Ruby são estruturas de dados que armazenam pares de chave-valor, per...
Meta Keywords: chave, ruby, que, valor, dados
-->

# Hash em Ruby: Estruturas de Dados Poderosas e Flexíveis

## Sinopse
Os Hashes em Ruby são estruturas de dados que armazenam pares de chave-valor, permitindo acesso eficiente e organizado a dados, facilitando a manipulação de informações.

## Documentação
### O que é um Hash?
Um Hash, também conhecido como dicionário ou mapa em outras linguagens de programação, é uma coleção de pares de chave-valor. As chaves devem ser únicas e imutáveis, enquanto os valores podem ser de qualquer tipo.

### Propósito
O propósito dos Hashes é permitir um armazenamento e recuperação rápida de dados. Eles são amplamente utilizados em Ruby para representar dados estruturados, como JSON ou configurações.

### Sintaxe
A sintaxe básica para criar um Hash é a seguinte:

```ruby
meu_hash = { chave1: 'valor1', chave2: 'valor2' }
```

### Métodos Comuns
- `#[]`: Acessa o valor associado a uma chave.
- `#[]=`: Atribui um valor a uma chave.
- `#each`: Itera sobre cada par chave-valor.
- `#keys`: Retorna um array com todas as chaves.
- `#values`: Retorna um array com todos os valores.

## Exemplos
### Criando um Hash
```ruby
carro = { marca: 'Toyota', modelo: 'Corolla', ano: 2020 }
```

### Acessando Valores
```ruby
puts carro[:marca] # Saída: Toyota
```

### Adicionando e Modificando Valores
```ruby
carro[:cor] = 'azul' # Adiciona nova chave
carro[:ano] = 2021   # Modifica o valor da chave existente
```

### Iterando sobre um Hash
```ruby
carro.each do |chave, valor|
  puts "#{chave}: #{valor}"
end
```

## Explicação
### Armadilhas Comuns
1. **Chaves Duplicadas**: Se você tentar adicionar uma chave que já existe, o valor anterior será sobrescrito, o que pode causar perda de dados.
2. **Tipos de Chave**: É importante lembrar que as chaves devem ser únicas e, normalmente, imutáveis (ex: símbolos ou strings).
3. **Acesso a Chave Não Existente**: Tentar acessar uma chave que não existe retornará `nil`, o que pode levar a erros se não for tratado corretamente.

### Notas Adicionais
- Hashes são mutáveis, o que significa que você pode alterar seu conteúdo após a criação.
- A ordem dos elementos é mantida desde Ruby 1.9, tornando os Hashes ainda mais úteis para armazenar dados em uma sequência específica.

## Resumo em Uma Linha
Hashes em Ruby são coleções de pares de chave-valor que oferecem uma maneira flexível e eficiente de armazenar e acessar dados.