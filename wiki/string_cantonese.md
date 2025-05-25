<!--
Meta Description: # Ruby 字串 (String) 的詳細介紹 ## 簡介 在 Ruby 語言中，字串（String）是一種用於儲存文本數據的基本數據類型。Ruby 提供了許多方法來操作字串，讓開發者可以輕鬆處理和變更文本內容。 ## 文檔 字串在 Ruby 中是一個可變的對象，這意味著可以在不創建新對象的情況下...
Meta Keywords: ruby, hello, greeting, world, puts
-->

# Ruby 字串 (String) 的詳細介紹

## 簡介
在 Ruby 語言中，字串（String）是一種用於儲存文本數據的基本數據類型。Ruby 提供了許多方法來操作字串，讓開發者可以輕鬆處理和變更文本內容。

## 文檔
字串在 Ruby 中是一個可變的對象，這意味著可以在不創建新對象的情況下修改字串內容。字串的主要用途包括但不限於文本顯示、數據處理、以及用於輸入輸出操作。

### 用法
在 Ruby 中，字串可以用單引號 (`'`) 或雙引號 (`"`) 來定義。兩者之間的主要區別是，雙引號中的插值和轉義字符會被解析，而單引號則不會。

```ruby
# 使用單引號
str1 = 'Hello, Ruby!'
# 使用雙引號
str2 = "Hello, #{str1}"
```

### 主要方法
- `length`: 返回字串的長度。
- `upcase`: 將字串轉換為大寫。
- `downcase`: 將字串轉換為小寫。
- `split`: 根據指定的分隔符將字串分割為數組。
- `gsub`: 替換字串中的指定內容。

## 範例
以下是一些基本的字串操作範例：

```ruby
# 定義字串
greeting = "Hello, World!"

# 獲取字串長度
puts greeting.length  # 輸出: 13

# 將字串轉換為大寫
puts greeting.upcase  # 輸出: HELLO, WORLD!

# 分割字串
words = greeting.split(", ")
puts words.inspect    # 輸出: ["Hello", "World!"]

# 替換字串中的內容
new_greeting = greeting.gsub("World", "Ruby")
puts new_greeting      # 輸出: Hello, Ruby!
```

## 說明
在使用 Ruby 字串時，開發者需要注意以下幾點常見的陷阱：

1. **插值與轉義**: 使用雙引號時，插值和轉義字符會生效，可能會導致意外的結果。
2. **不可變性**: 雖然 Ruby 字串是可變的，但某些方法（如 `upcase` 和 `downcase`）會返回新的字串，而不會改變原始字串。
3. **編碼問題**: 處理包含 Unicode 字符的字串時，可能會遇到編碼問題。確保使用正確的編碼來避免錯誤。

## 一句總結
Ruby 的字串類型是一個靈活且功能強大的工具，用於處理文本數據。