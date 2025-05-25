<!--
Meta Description: # Ruby 中的 `defined?`：用於檢查變量及方法的存在性 ## 概述 在 Ruby 編程語言中，`defined?` 是一個用於檢查變量、方法、類別或其他對象是否存在的關鍵字。它可以幫助開發者避免因為引用未定義的變量或方法而導致的錯誤。 ## 文檔 ### 目的 `defined?` 用...
Meta Keywords: defined, ruby, nil, puts, expression
-->

# Ruby 中的 `defined?`：用於檢查變量及方法的存在性

## 概述
在 Ruby 編程語言中，`defined?` 是一個用於檢查變量、方法、類別或其他對象是否存在的關鍵字。它可以幫助開發者避免因為引用未定義的變量或方法而導致的錯誤。

## 文檔
### 目的
`defined?` 用於檢查一個變量或方法是否已經被定義。這在動態語言中尤其有用，因為變量和方法可以在運行時創建或不存在。

### 用法
`defined?` 的語法如下：
```ruby
defined?(expression)
```

這裡的 `expression` 可以是任何 Ruby 表達式，包括變量名、方法名、類別名等。`defined?` 會返回一個字符串，指示該表達式的類型，或者返回 `nil` 如果該表達式沒有被定義。

### 詳細信息
- 返回值：
  - 如果表達式存在，`defined?` 會返回一個字符串，這個字符串描述了表達式的類型，例如 "local-variable"、"method"、"constant" 等。
  - 如果表達式不存在，則返回 `nil`。
  
- 注意，`defined?` 不會引發錯誤，即使該表達式是未定義的。

## 示例
以下是一些基本的 `defined?` 使用示例：

```ruby
# 檢查局部變量
x = 10
puts defined?(x) # 輸出 "local-variable"

# 檢查未定義的變量
puts defined?(y) # 輸出 nil

# 檢查方法
def my_method
end
puts defined?(my_method) # 輸出 "method"

# 檢查未定義的方法
puts defined?(undefined_method) # 輸出 nil
```

## 解釋
在使用 `defined?` 時，開發者應注意以下幾點：

- `defined?` 只會檢查名稱是否存在，而不會執行該表達式。如果您嘗試執行一個未定義的變量或方法，則會拋出錯誤。
- 儘管 `defined?` 可以用於檢查局部變量，但它不會檢查全局變量。如果需要檢查全局變量，應使用 `$` 前綴。
- 使用 `defined?` 時，應避免將其與其他邏輯或控制結構混合，因為這可能導致代碼的可讀性下降。

## 一句話總結
`defined?` 是 Ruby 中用於檢查變量或方法是否存在的關鍵字，能有效避免未定義錯誤。