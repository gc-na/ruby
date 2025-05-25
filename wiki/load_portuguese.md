<!--
Meta Description: # Carregamento de Arquivos em Ruby: Usando o Método `load` ## Sinopse O método `load` em Ruby é utilizado para carregar e executar um arquivo Ruby. El...
Meta Keywords: arquivo, load, ruby, que, método
-->

# Carregamento de Arquivos em Ruby: Usando o Método `load`

## Sinopse
O método `load` em Ruby é utilizado para carregar e executar um arquivo Ruby. Ele permite que os desenvolvedores reutilizem código de forma eficiente, permitindo a execução de scripts de forma dinâmica.

## Documentação
O método `load` tem como principal objetivo carregar um arquivo Ruby e executá-lo no contexto atual. Ao contrário do método `require`, que carrega um arquivo apenas uma vez, `load` pode ser chamado várias vezes para recarregar o mesmo arquivo.

### Propósito
- Carregar e executar arquivos Ruby.
- Permitir a recarga de um arquivo várias vezes durante a execução do programa.

### Uso
A sintaxe básica do método `load` é:

```ruby
load(file_name, wrap = false)
```

- `file_name`: O caminho para o arquivo Ruby que deve ser carregado. É uma string que pode ser um caminho absoluto ou relativo.
- `wrap`: Um parâmetro opcional que, se definido como `true`, encapsula a execução do arquivo em um bloco `begin/rescue`, permitindo capturar exceções lançadas.

### Detalhes
- O método `load` é útil em situações em que você precisa recarregar um arquivo, como durante o desenvolvimento, para refletir as alterações feitas no código.
- O arquivo carregado deve conter código Ruby válido. Se o código contiver erros, uma exceção será lançada.

## Exemplos
### Exemplo Básico
```ruby
# Supondo que você tenha um arquivo chamado 'script.rb' com o seguinte conteúdo:
# puts "Hello, World!"

load 'script.rb'
```
Saída:
```
Hello, World!
```

### Recarregando um Arquivo
```ruby
# Primeiro carregamento
load 'script.rb'  # Saída: Hello, World!

# Alterando o arquivo 'script.rb' para: puts "Hello novamente!"

# Recarregando
load 'script.rb'  # Saída: Hello novamente!
```

## Explicação
### Armadilhas Comuns
- **Caminhos Relativos**: Ao usar caminhos relativos, certifique-se de que o diretório atual está correto, pois isso pode causar `LoadError`.
- **Execução Múltipla**: Ao chamar `load` várias vezes, o código do arquivo será executado novamente, o que pode não ser desejado se o arquivo contém inicializações que não devem ser repetidas.
- **Erro de Sintaxe**: Se o arquivo contiver um erro de sintaxe, o `load` lançará uma exceção, o que pode interromper a execução do programa.

### Notas Adicionais
- Para evitar a recarga de arquivos já carregados, considere usar `require` para bibliotecas e módulos que não precisam ser recarregados frequentemente.
- O uso de `load` é mais comum em scripts e durante o desenvolvimento. Em produção, o uso de `require` é geralmente preferido.

## Resumo em uma Frase
O método `load` em Ruby permite carregar e executar arquivos Ruby dinamicamente, possibilitando a recarga de código durante a execução do programa.