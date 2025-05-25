<!--
Meta Description: # Ruby 中的符號 (Symbol) ## 概述 在 Ruby 中，符號（Symbol）是一種輕量級的、不可變的字串類型，通常用於標識和作為鍵名，因其性能優越而受到廣泛使用。 ## 文檔 符號是一種用冒號開頭的字串，例如 `:name`。在 Ruby 中，符號的主要用途是作為標識符，因為它們在內...
Meta Keywords: ruby, name, symbol, hash, hello
-->

# Ruby 中的符號 (Symbol)

## 概述
在 Ruby 中，符號（Symbol）是一種輕量級的、不可變的字串類型，通常用於標識和作為鍵名，因其性能優越而受到廣泛使用。

## 文檔
符號是一種用冒號開頭的字串，例如 `:name`。在 Ruby 中，符號的主要用途是作為標識符，因為它們在內存中是唯一的，並且不會創建新的實例。這意味著同一符號在程序中只佔用一個內存位置，這對於需要頻繁使用的標識符來說，可以節省內存並提高效率。

### 目的
符號主要用於：
- 作為 Hash 鍵
- 表示方法名
- 作為標識符傳遞給方法

### 用法
符號的創建非常簡單，只需在字串前加上冒號。例如：
```ruby
:name
```
可以直接使用符號來為 Hash 提供鍵名：
```ruby
person = { name: "John", age: 30 }
```

## 範例
以下是一些基本的符號用法示例：

### 創建符號
```ruby
symbol = :hello
puts symbol
```

### 作為 Hash 鍵
```ruby
user = { username: "alice", email: "alice@example.com" }
puts user[:username]  # 輸出 "alice"
```

### 方法命名
符號可以用於方法的名稱：
```ruby
def greet(name)
  "Hello, #{name}!"
end

method_name = :greet
puts send(method_name, "Bob")  # 輸出 "Hello, Bob!"
```

## 解釋
使用符號時有一些常見的陷阱需要注意：
- 符號是唯一的，因此在內存中是不可變的，這使得它們比字串更高效，但在需要動態改變的情況下，符號不合適。
- 不要將符號用作用戶輸入的標識符，因為這可能導致潛在的安全問題。

## 一句話總結
符號是 Ruby 中輕量級的、不可變的字串類型，通常用於標識和作為 Hash 鍵，因其內存效率高而廣泛使用。