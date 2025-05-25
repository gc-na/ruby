<!--
Meta Description: # Ruby中的「defined?」關鍵字詳細介紹 ## 概述 在Ruby編程中，「defined?」是一個關鍵字，用於檢查一個變量、方法、常量或其他對象是否已經被定義。這對於避免未定義的錯誤和提高代碼的健壯性至關重要。 ## 文檔 ### 目的 「defined?」關鍵字的主要目的是提供一種安全的...
Meta Keywords: defined, puts, nil, ruby, expression
-->

# Ruby中的「defined?」關鍵字詳細介紹

## 概述
在Ruby編程中，「defined?」是一個關鍵字，用於檢查一個變量、方法、常量或其他對象是否已經被定義。這對於避免未定義的錯誤和提高代碼的健壯性至關重要。

## 文檔
### 目的
「defined?」關鍵字的主要目的是提供一種安全的方式來檢查某個標識符（如變量或方法）是否存在，而不會引發錯誤。

### 用法
「defined?」的基本語法如下：

```ruby
defined?(expression)
```

這裡的 `expression` 可以是任何有效的Ruby表達式，如變量名、方法名或常量名。

### 返回值
- 返回一個描述標識符的字符串（例如，`"local-variable"`, `"method"`, `"constant"`等），如果標識符未定義，則返回 `nil`。

## 範例
### 基本用法示例

```ruby
# 檢查局部變量
x = 10
puts defined?(x)  # 輸出: "local-variable"

# 檢查未定義的變量
puts defined?(y)  # 輸出: nil

# 檢查方法
def my_method; end
puts defined?(my_method)  # 輸出: "method"

# 檢查常量
MY_CONSTANT = 100
puts defined?(MY_CONSTANT)  # 輸出: "constant"

# 檢查未定義的方法
puts defined?(undefined_method)  # 輸出: nil
```

## 解釋
### 常見陷阱和注意事項
- **作用域問題**：在不同的作用域中（如方法內部和外部），同一個變量可能會被定義或未定義。使用「defined?」時，必須考慮變量的作用域。
- **區分大小寫**：Ruby是區分大小寫的，因此 `my_variable` 和 `MY_VARIABLE` 是兩個不同的標識符。
- **無法檢查類別或模組的存在性**：對於類別或模組，如果希望檢查它們的存在性，應使用 `const_defined?` 方法。

## 總結
「defined?」是Ruby中用於檢查標識符是否存在的強大工具，有助於編寫更安全和可維護的代碼。