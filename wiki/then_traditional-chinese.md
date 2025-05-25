<!--
Meta Description: # Ruby 中的 `then` 關鍵字：用法與技巧 ## 摘要 `then` 是 Ruby 語言中的一個關鍵字，通常用於流控制結構中，例如在 `if` 語句後面作為一種替代語法，或在方法鏈中使用以增加可讀性。 ## 文檔 `then` 主要用來改善程式碼的可讀性，尤其是在需要多條語句的情況下。它的...
Meta Keywords: then, ruby, puts, array, end
-->

# Ruby 中的 `then` 關鍵字：用法與技巧

## 摘要
`then` 是 Ruby 語言中的一個關鍵字，通常用於流控制結構中，例如在 `if` 語句後面作為一種替代語法，或在方法鏈中使用以增加可讀性。

## 文檔
`then` 主要用來改善程式碼的可讀性，尤其是在需要多條語句的情況下。它的基本用法是在條件語句中，當條件成立時，執行一段程式碼。這使得程式碼更具結構性，並且可以讓開發者以更清晰的方式表達其意圖。

### 用法
在 Ruby 中，可以將 `then` 用於以下情境：

1. **在 `if` 條件語句中**：
   ```ruby
   if condition then
     # 執行的程式碼
   end
   ```

2. **與方法鏈結合使用**：
   ```ruby
   result = [1, 2, 3].map { |n| n * 2 }.then { |array| array.sum }
   ```

## 範例
以下是 `then` 的一些基本用法範例：

1. **基本的 `if` 使用**：
   ```ruby
   age = 18
   if age >= 18 then
     puts "你已經成年了！"
   end
   ```

2. **方法鏈中的使用**：
   ```ruby
   array = [1, 2, 3]
   result = array.map { |n| n * 2 }.then { |arr| arr.reduce(:+) }
   puts result  # 輸出：12
   ```

3. **搭配 `case` 語句**：
   ```ruby
   grade = 'A'
   case grade
   when 'A' then puts "優秀"
   when 'B' then puts "良好"
   else puts "需要進步"
   end
   ```

## 解釋
使用 `then` 時需要注意以下幾點：

- **可讀性**：雖然 `then` 增加了程式碼的可讀性，但過度使用可能導致混淆。應根據上下文選擇性使用。
- **語法限制**：`then` 必須正確地放置在條件後面，並且其後必須跟隨程式碼塊。
- **與其他控制結構的結合使用**：`then` 不僅限於 `if`，也可以在 `case` 語句中使用，這樣可以提高程式碼的整體結構性。

## 總結
`then` 是 Ruby 中一個有用的關鍵字，能夠提高程式碼的可讀性和結構性。