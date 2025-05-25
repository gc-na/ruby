<!--
Meta Description: # Ruby 中的 "or" 操作符使用指南 ## 概述 "or" 是 Ruby 中的一個邏輯運算符，用於在條件判斷中連接兩個布林表達式。當其中一個表達式為真時，"or" 會返回真。 ## 文檔 ### 目的 "or" 操作符主要用於控制流結構，例如條件語句，讓程式能根據不同的條件執行不同的代碼。 ...
Meta Keywords: ruby, true, result, condition1, condition2
-->

# Ruby 中的 "or" 操作符使用指南

## 概述
"or" 是 Ruby 中的一個邏輯運算符，用於在條件判斷中連接兩個布林表達式。當其中一個表達式為真時，"or" 會返回真。

## 文檔
### 目的
"or" 操作符主要用於控制流結構，例如條件語句，讓程式能根據不同的條件執行不同的代碼。

### 用法
在 Ruby 中，"or" 的基本語法如下：
```ruby
condition1 or condition2
```
如果 `condition1` 為真，則整個表達式返回真；如果 `condition1` 為假，則返回 `condition2` 的結果。

### 詳細
- 優先順序：在 Ruby 中，"or" 的優先順序低於大多數其他運算符，特別是 "and"。這意味著在複雜的表達式中，使用括號來明確運算順序是非常重要的。
- 短路求值：如果 `condition1` 為真，則 Ruby 不會評估 `condition2`，這可以用於防止不必要的計算或運行代碼。

## 示例
下面是一些使用 "or" 的基本示例：

### 示例 1：基本使用
```ruby
a = true
b = false

result = a or b
puts result  # 輸出: true
```

### 示例 2：條件判斷
```ruby
user_input = nil
default_value = "default"

value = user_input or default_value
puts value  # 輸出: default
```

### 示例 3：短路求值
```ruby
def risky_operation
  puts "Risky operation executed!"
  return true
end

result = false or risky_operation
# 輸出: 不會執行 "Risky operation executed!"
```

## 解釋
### 常見陷阱
1. **優先順序問題**：由於 "or" 的優先順序低於其他運算符，確保使用括號來避免意外的邏輯錯誤。
   ```ruby
   # 錯誤示例
   result = true or false  # 這樣 result 始終會是 true
   ```

2. **與 "||" 的區別**：Ruby 中還有一個更常用的邏輯運算符 "||"，其優先順序高於 "or"，並且通常在需要控制流時使用。選擇使用哪個操作符要根據上下文決定。

### 附加說明
在需要進行布林邏輯運算時，選擇正確的運算符對於程式的可讀性和性能是至關重要的。根據需求選擇 "or" 或 "||"，並注意它們在短路求值和優先順序上的差異。

## 一句總結
Ruby 中的 "or" 操作符用於連接布林表達式，當至少一個為真時返回真，並具有短路求值的特性。