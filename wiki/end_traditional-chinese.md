<!--
Meta Description: # Ruby 中的 "end" 關鍵字：結束語句的核心 ## 摘要 在 Ruby 程式語言中，`end` 是一個關鍵字，用於標識程式碼區塊的結束，通常與控制結構（如方法、類別、模組、條件語句、迴圈等）結合使用。它是 Ruby 語法的核心部分，對於正確結束程式碼區塊至關重要。 ## 文檔 ### 目的...
Meta Keywords: end, ruby, def, puts, make
-->

# Ruby 中的 "end" 關鍵字：結束語句的核心

## 摘要
在 Ruby 程式語言中，`end` 是一個關鍵字，用於標識程式碼區塊的結束，通常與控制結構（如方法、類別、模組、條件語句、迴圈等）結合使用。它是 Ruby 語法的核心部分，對於正確結束程式碼區塊至關重要。

## 文檔
### 目的
`end` 關鍵字的主要目的是明確地標記出程式碼區塊的結束。Ruby 是一種以縮排為基礎的語言，但結束關鍵字的使用使得程式碼的結構更加清晰和可讀。

### 用法
在 Ruby 中，`end` 用於各種語法結構中，包括：

- 方法定義
- 類別定義
- 模組定義
- 條件語句（如 `if`, `unless`, `case`）
- 迴圈（如 `while`, `until`, `for`）

### 詳細說明
在 Ruby 中，`end` 必須與相應的開頭關鍵字配對，這樣才能正確解析程式碼。例如，當你定義一個方法時，必須在方法的結尾使用 `end` 來標示結束。

以下是一些基本的語法結構示例：

- 方法定義：
  ```ruby
  def greet
    puts "Hello, World!"
  end
  ```

- 類別定義：
  ```ruby
  class Animal
    def speak
      puts "Roar!"
    end
  end
  ```

- 條件語句：
  ```ruby
  if true
    puts "This is true."
  end
  ```

## 範例
### 範例 1：方法定義
```ruby
def add(a, b)
  return a + b
end

puts add(2, 3)  # 輸出 5
```

### 範例 2：類別定義
```ruby
class Car
  def initialize(make, model)
    @make = make
    @model = model
  end

  def info
    puts "Make: #{@make}, Model: #{@model}"
  end
end

my_car = Car.new("Toyota", "Corolla")
my_car.info  # 輸出 "Make: Toyota, Model: Corolla"
```

### 範例 3：條件語句
```ruby
number = 10
if number > 5
  puts "Number is greater than 5."
end
```

## 解釋
在使用 `end` 時，開發者需要注意以下幾點：

1. **配對結構**：確保每一個開頭結構（如 `def`, `class`, `if` 等）都有一個對應的 `end`。如果缺少了 `end`，Ruby 將會報錯。

2. **嵌套結構**：在使用嵌套的情況下，確保 `end` 的數量與開頭結構相匹配，以避免語法錯誤。

3. **可讀性**：良好的縮排和適當的註解可以提高程式碼的可讀性，幫助其他開發者理解程式碼的結構。

## 一句總結
在 Ruby 中，`end` 是一個關鍵字，用於標記程式碼區塊的結束，對於維護結構清晰的程式碼至關重要。