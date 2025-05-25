<!--
Meta Description: # Ruby 中的 "then" 關鍵字：用法與示例 ## 摘要 "then" 是 Ruby 語言中的一個關鍵字，主要用於改善程式碼的可讀性，特別是在條件語句中。 ## 文檔 在 Ruby 中，"then" 是一個選擇性的關鍵字，通常在 `if`、`case` 和 `unless` 語句中使用。當我...
Meta Keywords: then, ruby, end, case, unless
-->

# Ruby 中的 "then" 關鍵字：用法與示例

## 摘要
"then" 是 Ruby 語言中的一個關鍵字，主要用於改善程式碼的可讀性，特別是在條件語句中。

## 文檔
在 Ruby 中，"then" 是一個選擇性的關鍵字，通常在 `if`、`case` 和 `unless` 語句中使用。當我們需要在條件語句後面緊接著一個區塊時，可以使用 "then" 來分隔條件和區塊，提高程式碼的清晰度。

### 用法
"then" 可以在以下情況中使用：

1. **if 語句**:
   ```ruby
   if condition then
     # 執行的程式碼
   end
   ```

2. **case 語句**:
   ```ruby
   case variable
   when value1 then
     # 執行的程式碼
   end
   ```

3. **unless 語句**:
   ```ruby
   unless condition then
     # 執行的程式碼
   end
   ```

## 示例
以下是一些基本的使用示例：

### 示例 1：使用 if 語句
```ruby
x = 10
if x > 5 then
  puts "x 大於 5"
end
```

### 示例 2：使用 case 語句
```ruby
grade = 'A'
case grade
when 'A' then
  puts "優秀"
when 'B' then
  puts "良好"
else
  puts "需要改進"
end
```

### 示例 3：使用 unless 語句
```ruby
y = 3
unless y > 5 then
  puts "y 小於或等於 5"
end
```

## 解釋
雖然 "then" 是可選的，但在某些情況下使用 "then" 可以使程式碼更易於閱讀。特別是在複雜的條件語句中，使用 "then" 可以幫助開發者快速定位條件和執行的程式碼塊。

### 常見陷阱
- 在 Ruby 中，"then" 並不是必須的，因此許多開發者可能會選擇省略它。在簡單的條件語句中，省略 "then" 不會影響程式碼的功能，但可能會影響可讀性。
- 使用 "then" 時，確保它與正確的條件語句配對，否則會導致語法錯誤或預期外的行為。

## 一句總結
"then" 是 Ruby 中一個用於提高條件語句可讀性的關鍵字，雖然是可選的，但在適當的情況下使用可以使程式碼更清晰。