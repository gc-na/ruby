<!--
Meta Description: # Ruby 的 else 關鍵字：用法與範例 ## 概要 在 Ruby 中，`else` 關鍵字用於條件語句的控制結構中，與 `if`、`elsif` 一起使用，提供了一種在所有先前條件不成立時執行的操作方式。 ## 文件說明 `else` 是 Ruby 中的一個關鍵字，主要用於條件判斷結構中。當...
Meta Keywords: else, ruby, elsif, puts, end
-->

# Ruby 的 else 關鍵字：用法與範例

## 概要
在 Ruby 中，`else` 關鍵字用於條件語句的控制結構中，與 `if`、`elsif` 一起使用，提供了一種在所有先前條件不成立時執行的操作方式。

## 文件說明
`else` 是 Ruby 中的一個關鍵字，主要用於條件判斷結構中。當使用 `if` 語句或 `case` 語句時，`else` 提供了一個後備選項，允許開發者在所有其他條件均不滿足的情況下執行特定的程式碼區塊。

### 目的
`else` 的主要目的是在多條件判斷中，當沒有任何條件成立時提供一個默認的執行路徑，這有助於提高程式的可讀性和可維護性。

### 使用方式
`else` 的基本語法如下：
```ruby
if condition1
  # 當 condition1 為 true 時執行的程式碼
elsif condition2
  # 當 condition2 為 true 時執行的程式碼
else
  # 當上述條件均不成立時執行的程式碼
end
```

## 範例
以下是 `else` 的基本用法範例：

### 範例 1：簡單的 if-else 結構
```ruby
age = 18

if age < 18
  puts "未成年人"
else
  puts "成年人"
end
```
輸出：
```
成年人
```

### 範例 2：使用 elsif 和 else
```ruby
score = 75

if score >= 90
  puts "優秀"
elsif score >= 75
  puts "良好"
else
  puts "需加強"
end
```
輸出：
```
良好
```

## 解釋
在使用 `else` 時，有幾個常見的陷阱和注意事項：

1. **語法錯誤**：確保 `else` 之前有相應的 `if` 或 `elsif`，否則會出現語法錯誤。
2. **不必要的 else**：在某些情況下，可能不需要使用 `else`，特別是當所有情況都已經被涵蓋時。
3. **可讀性**：適當使用 `else` 可以提高程式碼的可讀性，但過度複雜的條件結構可能會使程式碼難以理解。

## 一句總結
`else` 在 Ruby 中是一個關鍵字，用於提供在所有條件不成立時的默認執行路徑。