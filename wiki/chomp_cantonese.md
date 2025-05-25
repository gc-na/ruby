<!--
Meta Description: # Ruby 中的 chomp 方法：去除字串末尾的換行符 ## 簡介 在 Ruby 中，`chomp` 方法是一個用來去除字串末尾換行符的簡單而有效的工具，特別是在處理用戶輸入或文件讀取時。 ## 文件說明 ### 目的 `chomp` 方法的主要目的是清除字串末尾的換行符（如 `\n` 或 `\...
Meta Keywords: chomp, ruby, line, hello, world
-->

# Ruby 中的 chomp 方法：去除字串末尾的換行符

## 簡介
在 Ruby 中，`chomp` 方法是一個用來去除字串末尾換行符的簡單而有效的工具，特別是在處理用戶輸入或文件讀取時。

## 文件說明
### 目的
`chomp` 方法的主要目的是清除字串末尾的換行符（如 `\n` 或 `\r\n`），使得處理字串時更加方便。

### 使用方法
`chomp` 方法可以被用於任何 Ruby 字串對象。基本語法如下：

```ruby
string.chomp(separator)
```

- `separator` 是可選的，指定要去除的結尾字符，預設為換行符。

### 詳細說明
- 如果字串的最後一個字符是指定的分隔符，`chomp` 方法將其去除並返回新字串。
- 若字串的末尾不是分隔符，則返回原字串。
- `chomp` 方法不會修改原有的字串，而是返回一個新的字串。

## 示例
### 示例 1: 基本用法
```ruby
line = "Hello, World!\n"
cleaned_line = line.chomp
puts cleaned_line  # 輸出: Hello, World!
```

### 示例 2: 指定分隔符
```ruby
line = "Hello, World!\r\n"
cleaned_line = line.chomp("\r\n")
puts cleaned_line  # 輸出: Hello, World!
```

### 示例 3: 沒有分隔符的情況
```ruby
line = "Hello, World!"
cleaned_line = line.chomp
puts cleaned_line  # 輸出: Hello, World!
```

## 解釋
- **常見錯誤**: 初學者可能會誤以為 `chomp` 會修改原字串，但其實它會返回一個新字串。
- **注意事項**: 使用 `chomp` 時，需了解它只會去除字串末尾的分隔符，對於字串中間的內容不會有影響。

## 一句總結
`chomp` 方法在 Ruby 中用於方便地去除字串末尾的換行符，確保字串處理更為簡潔有效。