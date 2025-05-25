<!--
Meta Description: # Ruby 中的 "end" 關鍵字：結束區塊的基石 ## 概述 在 Ruby 編程語言中，`end` 是一個關鍵字，用於標示區塊、方法、類別和模塊的結束。它是 Ruby 語法的一部分，使得程式碼結構清晰易讀。 ## 文檔 `end` 關鍵字的主要目的在於結束一個開啟的區塊。在 Ruby 中，許多...
Meta Keywords: end, ruby, puts, def, 來結束
-->

# Ruby 中的 "end" 關鍵字：結束區塊的基石

## 概述
在 Ruby 編程語言中，`end` 是一個關鍵字，用於標示區塊、方法、類別和模塊的結束。它是 Ruby 語法的一部分，使得程式碼結構清晰易讀。

## 文檔
`end` 關鍵字的主要目的在於結束一個開啟的區塊。在 Ruby 中，許多結構（如方法、類別、模塊、條件語句和迴圈）都是以 `do` 或其他關鍵字開頭，並需要用 `end` 來結束。這不僅有助於程式碼的可讀性，還能避免語法錯誤。

### 用法
- **結束方法**：每當定義一個方法時，必須以 `end` 來結束。例如：
  ```ruby
  def say_hello
    puts "Hello, World!"
  end
  ```

- **結束類別**：類別定義也需要以 `end` 來結束。例如：
  ```ruby
  class Animal
    def speak
      puts "Animal speaks"
    end
  end
  ```

- **結束模塊**：模塊的定義同樣需要用 `end` 來結束。例如：
  ```ruby
  module MyModule
    def my_method
      puts "Hello from MyModule"
    end
  end
  ```

- **結束條件語句**：在使用 `if`、`unless` 等條件語句時，也需以 `end` 結束。例如：
  ```ruby
  if true
    puts "This is true"
  end
  ```

- **結束迴圈**：迴圈如 `while` 和 `until` 也需要 `end` 來標示結束。例如：
  ```ruby
  while true
    puts "Looping"
    break
  end
  ```

## 範例
以下是一些簡單的範例，展示了 `end` 的使用：

1. **方法定義**：
   ```ruby
   def greet(name)
     puts "Hello, #{name}!"
   end
   ```

2. **類別定義**：
   ```ruby
   class Car
     def initialize(make, model)
       @make = make
       @model = model
     end
   end
   ```

3. **模塊定義**：
   ```ruby
   module MathOperations
     def self.add(a, b)
       a + b
     end
   end
   ```

4. **條件語句**：
   ```ruby
   number = 10
   if number > 5
     puts "Number is greater than 5"
   end
   ```

5. **迴圈**：
   ```ruby
   count = 0
   until count == 5
     puts count
     count += 1
   end
   ```

## 解釋
使用 `end` 時常見的陷阱包括：
- 忘記加上 `end` 會導致語法錯誤，Ruby 會提示你缺少結束的標記。
- 在嵌套結構中，可能會混淆哪個 `end` 對應哪個開啟的區塊，因此建議注意縮排以提高可讀性。
- 在使用 `do...end` 與 `{...}` 時，保持一致性以避免混淆。

## 總結
`end` 是 Ruby 中關鍵的結束標記，用於結束方法、類別、模塊及其他區塊結構。