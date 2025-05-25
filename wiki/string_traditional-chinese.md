<!--
Meta Description: # Ruby 字串 (String) 的完整指南 ## 摘要 Ruby 的字串 (String) 是一種非常重要的資料類型，用於儲存和操作文字數據。它提供了多種方法來處理和操作字串，使得開發者能夠輕鬆地進行文字處理。 ## 文檔 在 Ruby 中，字串是一種可變的對象，代表一系列的字符。字串可以用單...
Meta Keywords: ruby, str, hello, world, str2
-->

# Ruby 字串 (String) 的完整指南

## 摘要
Ruby 的字串 (String) 是一種非常重要的資料類型，用於儲存和操作文字數據。它提供了多種方法來處理和操作字串，使得開發者能夠輕鬆地進行文字處理。

## 文檔
在 Ruby 中，字串是一種可變的對象，代表一系列的字符。字串可以用單引號 `''` 或雙引號 `""` 來定義。雖然兩者都能創建字串，但雙引號允許插入特殊字符和變數。

### 目的
字串的主要目的是提供一種方式來儲存和操作文字數據，使開發者能夠方便地進行文字處理操作，例如連接、切割、替換和查詢。

### 用法
- 創建字串：`str = "Hello, World!"`
- 訪問字串的字符：`str[0]` 會返回 `'H'`
- 字串長度：`str.length` 或 `str.size`
- 字串連接：`str1 + str2` 或 `str1.concat(str2)`

### 詳細信息
Ruby 的字串提供了許多內建方法，例如：
- `upcase`：將字串轉換為大寫。
- `downcase`：將字串轉換為小寫。
- `strip`：移除字串前後的空格。
- `gsub`：用於替換字串中的部分內容。
- `include?`：檢查字串是否包含某個子字串。

## 範例
```ruby
# 創建字串
str = "Hello, World!"

# 訪問字符
puts str[0]         # 輸出: H

# 字串長度
puts str.length     # 輸出: 13

# 字串連接
str2 = " How are you?"
combined = str + str2
puts combined       # 輸出: Hello, World! How are you?

# 替換字串
replaced = str.gsub("World", "Ruby")
puts replaced       # 輸出: Hello, Ruby!
```

## 解釋
使用字串時，開發者應注意以下幾點：
- 使用單引號時，無法插入變數或特殊字符（如換行符），而雙引號則可以。
- 字串是可變的，這意味著可以在原地修改字串，但這也可能導致意外的副作用。
- Ruby 的字串是 Unicode 支持的，這使得它能夠處理多語言內容，但在某些操作中可能需考慮字符編碼問題。

## 一句話總結
Ruby 的字串是一種靈活且功能強大的資料類型，用於儲存和操作文字數據。