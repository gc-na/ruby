<!--
Meta Description: # Manipulação de Arquivos em Ruby: Entenda a Classe File ## Sinopse A classe `File` em Ruby proporciona uma interface robusta para a manipulação de ar...
Meta Keywords: file, arquivos, arquivo, ruby, classe
-->

# Manipulação de Arquivos em Ruby: Entenda a Classe File

## Sinopse
A classe `File` em Ruby proporciona uma interface robusta para a manipulação de arquivos, permitindo operações como leitura, escrita, e gerenciamento de atributos de arquivos de forma simples e eficiente.

## Documentação
A classe `File` é uma parte essencial da biblioteca padrão do Ruby, utilizada para interagir com o sistema de arquivos. Com ela, é possível abrir, ler, escrever e fechar arquivos, além de modificar permissões e verificar a existência de arquivos.

### Propósito
O propósito da classe `File` é fornecer uma maneira simples de realizar operações de entrada e saída (I/O) em arquivos, facilitando tarefas comuns como a leitura de dados de um arquivo, a gravação de informações, e a manipulação de arquivos existentes.

### Uso
Para utilizar a classe `File`, você pode abri-la utilizando o método `File.open`, que permite especificar o modo de acesso (como leitura, escrita, ou adição). Abaixo estão alguns modos de acesso comuns:
- `"r"`: Leitura (padrão).
- `"w"`: Escrita (cria um novo arquivo ou sobrescreve um existente).
- `"a"`: Adição (escreve no final do arquivo).

### Detalhes
- **Fechamento de Arquivos**: É importante fechar arquivos após a utilização para liberar recursos. O método `close` deve ser chamado, ou você pode usar um bloco com `File.open`, que garante que o arquivo seja fechado automaticamente.
- **Tratamento de Erros**: Sempre que possível, utilize blocos `begin-rescue` para tratar erros ao trabalhar com arquivos, como arquivos não encontrados ou erros de permissão.

## Exemplos
Aqui estão alguns exemplos simples de como utilizar a classe `File`:

### Exemplo 1: Leitura de um Arquivo
```ruby
File.open("exemplo.txt", "r") do |file|
  file.each_line do |line|
    puts line
  end
end
```

### Exemplo 2: Escrita em um Arquivo
```ruby
File.open("exemplo.txt", "w") do |file|
  file.puts "Olá, Ruby!"
end
```

### Exemplo 3: Adição a um Arquivo
```ruby
File.open("exemplo.txt", "a") do |file|
  file.puts "Adicionando uma nova linha."
end
```

## Explicação
Um dos erros comuns ao usar a classe `File` é esquecer de fechar um arquivo após a sua utilização, o que pode causar vazamento de recursos. Além disso, ao trabalhar com arquivos, é crucial verificar se o arquivo existe antes de tentar abri-lo, para evitar exceções.

Outra armadilha é não considerar o modo de abertura do arquivo; por exemplo, usar `"w"` sobrescreverá qualquer conteúdo existente no arquivo. Portanto, sempre revise o modo de operação antes de abrir um arquivo.

## Resumo em Uma Linha
A classe `File` em Ruby fornece uma interface simplificada para a manipulação de arquivos, permitindo operações de leitura e escrita de maneira eficiente e intuitiva.