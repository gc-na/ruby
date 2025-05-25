<!--
Meta Description: # Ruby 中的 case 語句：用於控制流程的強大工具 ## 簡介 在 Ruby 程式語言中，`case` 語句是一種用於控制流程的結構，能夠根據不同的條件執行相應的代碼塊。它提供了一種清晰且易於閱讀的方式來處理多個條件，特別是在面對多個 `if` 和 `elsif` 語句時。 ## 文件說明 ...
Meta Keywords: when, case, puts, ruby, else
-->

# Ruby 中的 case 語句：用於控制流程的強大工具

## 簡介
在 Ruby 程式語言中，`case` 語句是一種用於控制流程的結構，能夠根據不同的條件執行相應的代碼塊。它提供了一種清晰且易於閱讀的方式來處理多個條件，特別是在面對多個 `if` 和 `elsif` 語句時。

## 文件說明
`case` 語句的主要目的是簡化多條件的判斷邏輯。它的基本語法如下：

```ruby
case 表達式
when 條件1
  # 當表達式等於條件1 時執行的代碼
when 條件2
  # 當表達式等於條件2 時執行的代碼
else
  # 當沒有匹配的條件時執行的代碼
end
```

### 使用方法
1. **表達式** - 是要進行比較的對象。
2. **when** - 用於定義要匹配的條件。可以有多個 `when` 子句。
3. **else** - 是可選的，當沒有任何 `when` 條件符合時執行的代碼。

## 範例
以下是一些基本用法的示例：

### 範例 1：簡單的 case 語句

```ruby
number = 2

case number
when 1
  puts "數字是 1"
when 2
  puts "數字是 2"
when 3
  puts "數字是 3"
else
  puts "數字不在範圍內"
end
```

### 範例 2：使用範圍

```ruby
grade = 85

case grade
when 90..100
  puts "優秀"
when 80..89
  puts "良好"
when 70..79
  puts "及格"
else
  puts "不及格"
end
```

### 範例 3：以表達式作為條件

```ruby
value = 'apple'

case value
when 'apple', 'banana'
  puts "這是一種水果"
when 'carrot'
  puts "這是一種蔬菜"
else
  puts "未知類型"
end
```

## 解釋
在使用 `case` 語句時，開發者需注意以下幾點：

- **類型匹配**：`case` 語句進行的是嚴格匹配，這意味著類型必須一致。
- **多個條件**：使用逗號可以在一個 `when` 語句中匹配多個條件，但所有條件必須相同類型。
- **else 是可選的**：如果沒有提供 `else`，而所有條件都不匹配，則不會執行任何代碼，這在某些情況下可能會導致意外行為。

## 一句總結
Ruby 中的 `case` 語句是一種清晰且高效的方式來處理多重條件的控制流程。