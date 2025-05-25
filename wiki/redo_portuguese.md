<!--
Meta Description: # Redo: Comando do Ruby para Repetição de Blocos ## Sinopse O comando `redo` em Ruby é utilizado para repetir a execução do bloco de código em loops e...
Meta Keywords: redo, contador, bloco, que, comando
-->

# Redo: Comando do Ruby para Repetição de Blocos

## Sinopse
O comando `redo` em Ruby é utilizado para repetir a execução do bloco de código em loops e estruturas de controle como `begin-rescue`. Isso permite que o programador retorne ao início do bloco em vez de recomeçar a execução do loop ou sair do bloco, sendo útil em situações de tratamento de erros.

## Documentação
O `redo` é um comando que pode ser utilizado dentro de estruturas de controle como `while`, `until`, `for` e `begin-rescue`. Ele não deve ser confundido com o comando `retry`, que reinicia uma operação de captura de exceções.

### Propósito
O propósito do comando `redo` é fornecer uma maneira de repetir a execução de um bloco de código após uma condição específica. Esse comando é especialmente útil quando você deseja tentar executar novamente um trecho de código que falhou, sem sair do contexto do loop ou do bloco.

### Uso
A sintaxe básica do `redo` é a seguinte:

```ruby
redo
```

### Detalhes
- O `redo` deve ser utilizado dentro de um bloco que já está em execução.
- Ele não pode ser utilizado fora de um bloco de controle e gera um erro se tentado.
- O `redo` não reinicia a execução do loop, mas sim do bloco em que está contido.

## Exemplos

### Exemplo 1: Uso básico do `redo`
```ruby
contador = 0

while contador < 5
  contador += 1
  puts "Contador: #{contador}"

  if contador == 3
    puts "Refazendo a iteração quando contador é 3."
    redo
  end
end
```
**Saída:**
```
Contador: 1
Contador: 2
Contador: 3
Refazendo a iteração quando contador é 3.
Contador: 3
Contador: 4
Contador: 5
```

### Exemplo 2: Uso do `redo` em um bloco `begin-rescue`
```ruby
def divisao(a, b)
  begin
    resultado = a / b
    puts "Resultado: #{resultado}"
  rescue ZeroDivisionError
    puts "Divisão por zero. Tentando novamente."
    b = 1  # Alterando o divisor
    redo
  end
end

divisao(10, 0)
```
**Saída:**
```
Divisão por zero. Tentando novamente.
Resultado: 10
```

## Explicação
O uso do `redo` pode levar a loops infinitos se não houver uma condição que permita a saída do bloco. É importante certificar-se de que a condição que leva ao `redo` será eventualmente satisfeita. Outro ponto a ser observado é que o `redo` não pode ser utilizado fora de um contexto de loop ou bloco, o que resultará em um erro de execução.

## Resumo em uma linha
O comando `redo` em Ruby permite repetir a execução de um bloco de código dentro de loops ou estruturas de controle, sem sair do contexto atual.