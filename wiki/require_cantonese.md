<!--
Meta Description: # Ruby 中的 require 指令：載入外部程式庫的關鍵 ## 簡介 在 Ruby 程式設計中，`require` 是一個用於載入外部程式庫或 Ruby 檔案的命令。此指令使開發者能夠重用代碼，提升開發效率並保持代碼的整潔。 ## 文檔 `require` 指令的主要目的是引入外部的 Ruby...
Meta Keywords: require, ruby, json, name, greetings
-->

# Ruby 中的 require 指令：載入外部程式庫的關鍵

## 簡介
在 Ruby 程式設計中，`require` 是一個用於載入外部程式庫或 Ruby 檔案的命令。此指令使開發者能夠重用代碼，提升開發效率並保持代碼的整潔。

## 文檔
`require` 指令的主要目的是引入外部的 Ruby 檔案或庫，以便在當前程式中使用其功能。當你使用 `require` 時，Ruby 會搜索指定的檔案並載入其內容，這樣你就可以使用該檔案中定義的類、模組和方法。

### 用法
基本的用法如下：
```ruby
require '檔案名稱'
```
這裡的 '檔案名稱' 可以是 Ruby 標準庫中的名稱，如 `json`、`net/http`，或者是你的自定義檔案名稱（不需要 .rb 副檔名）。

### 詳細說明
- `require` 會檢查檔案是否已經被載入過，如果已經載入，則不會重複載入，這樣可以避免重複定義的錯誤。
- 若檔案未能找到，`require` 會拋出一個 `LoadError` 例外。
- `require_relative` 是 `require` 的一個變體，允許你載入與當前檔案相對路徑的檔案。

## 範例
以下是使用 `require` 的幾個基本範例：

### 例子 1：載入標準庫
```ruby
require 'json'

data = { name: "Alice", age: 30 }
json_data = JSON.generate(data)
puts json_data
```

### 例子 2：載入自定義檔案
假設有一個名為 `greetings.rb` 的檔案：
```ruby
# greetings.rb
def greet(name)
  "你好，#{name}！"
end
```
可以這樣載入並使用：
```ruby
require './greetings'

puts greet("小明")
```

## 解釋
在使用 `require` 時，開發者應注意以下幾點：
- 確保指定的檔案路徑正確，否則會導致 `LoadError`。
- 如果需要載入位於不同目錄的檔案，可以利用 `require_relative` 指令。
- 使用全名載入標準庫時，無需加上 `.rb` 副檔名。

## 總結
`require` 是 Ruby 中一個不可或缺的指令，用於載入和重用外部程式庫或檔案，使得程式設計更為高效。