<!--
Meta Description: # Rubyのreturn文: 戻り値を制御する方法 ## 概要 Rubyにおける`return`文は、メソッドから値を返すために使用される重要な構文です。このコマンドを使用することで、メソッドの実行結果を呼び出し元に返すことができます。 ## ドキュメンテーション `return`文は、メソッドの...
Meta Keywords: return, puts, check_number, ruby, def
-->

# Rubyのreturn文: 戻り値を制御する方法

## 概要
Rubyにおける`return`文は、メソッドから値を返すために使用される重要な構文です。このコマンドを使用することで、メソッドの実行結果を呼び出し元に返すことができます。

## ドキュメンテーション
`return`文は、メソッドの実行を終了し、指定された値を呼び出し元に返します。Rubyでは、メソッドが明示的に戻り値を返さない場合、最後に評価された式の値が自動的に返されますが、`return`を使用することで、明確に戻り値を指定することができます。

### 用法
`return`文は、次のように使用します:

```ruby
def メソッド名
  # 処理
  return 戻り値
end
```

### 詳細
- `return`文は、メソッド内で任意の位置に配置できますが、メソッドが呼び出されるたびにその位置で処理が終了します。
- 値を返さずに`return`を記述した場合、`nil`が返されます。
- `return`はブロックやProc内でも使用できますが、その場合はブロックやProcのスコープに影響を与えます。

## 例
以下は、`return`文の基本的な使用例です。

```ruby
def add(a, b)
  return a + b
end

result = add(2, 3)  # resultは5になります
puts result
```

別の例では、条件に基づいて異なる戻り値を返します。

```ruby
def check_number(num)
  return "Positive" if num > 0
  return "Negative" if num < 0
  return "Zero"
end

puts check_number(5)   # "Positive"
puts check_number(-3)  # "Negative"
puts check_number(0)   # "Zero"
```

## 説明
`return`文を誤用すると、意図しない動作を引き起こすことがあります。特に、メソッド内で複数回`return`を使用する場合、どの`return`が実行されるか注意が必要です。また、ブロック内で`return`を使用すると、親メソッドから戻ることになるため、意図しない結果を招くことがあります。これを避けるために、ブロック内では`next`を使用することを検討してください。

## 一文の要約
Rubyにおける`return`文は、メソッドから値を明示的に返すために使用される構文です。