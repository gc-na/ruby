<!--
Meta Description: # Ruby Enumerable 模組：深入了解 Ruby 的枚舉功能 ## 摘要 Enumerable 是 Ruby 中一個強大的模組，提供了一系列的迭代器和查詢方法，讓開發者能夠方便地操作集合類型（如 Array 和 Hash）。它使得在這些集合上進行搜尋、排序和其他操作變得更加簡單和直觀。 ...
Meta Keywords: num, enumerable, ruby, puts, map
-->

# Ruby Enumerable 模組：深入了解 Ruby 的枚舉功能

## 摘要
Enumerable 是 Ruby 中一個強大的模組，提供了一系列的迭代器和查詢方法，讓開發者能夠方便地操作集合類型（如 Array 和 Hash）。它使得在這些集合上進行搜尋、排序和其他操作變得更加簡單和直觀。

## 文檔
### 目的
Enumerable 模組的主要目的是提供集合操作的統一接口，讓開發者能夠以簡潔的方式對集合進行各種操作，如遍歷、過濾和修改。

### 使用
Enumerable 模組並不能直接實例化，而是通常被包括在其他類別中，例如 Array 和 Hash。要使用 Enumerable 的方法，您只需在這些類別中調用即可。

### 主要方法
- `each`: 遍歷集合中的每個元素。
- `map`: 對每個元素應用給定的區塊，並返回一個新陣列。
- `select`: 選擇符合條件的元素，返回一個新陣列。
- `reject`: 選擇不符合條件的元素，返回一個新陣列。
- `reduce`: 將集合中的元素進行累加或其他操作。

## 範例
```ruby
# 使用 each 遍歷陣列
[1, 2, 3].each do |num|
  puts num
end

# 使用 map 將每個元素平方
squared = [1, 2, 3].map { |num| num ** 2 }
puts squared # => [1, 4, 9]

# 使用 select 選擇偶數
evens = [1, 2, 3, 4, 5].select { |num| num.even? }
puts evens # => [2, 4]

# 使用 reject 選擇非偶數
odds = [1, 2, 3, 4, 5].reject { |num| num.even? }
puts odds # => [1, 3, 5]

# 使用 reduce 計算總和
sum = [1, 2, 3, 4].reduce(0) { |acc, num| acc + num }
puts sum # => 10
```

## 解釋
使用 Enumerable 模組時，開發者應注意以下幾點：
- 確保集合類別已包含 Enumerable 模組，否則相應的方法將無法使用。
- 在使用 `map` 和 `select` 方法時，確保區塊的返回值正確，以避免獲得意外的結果。
- `reduce` 方法的初始值是可選的，若不提供，將使用集合中的第一個元素作為初始值，此時對於空集合將會引發錯誤。

## 總結
Enumerable 模組提供了強大且靈活的工具，讓 Ruby 開發者能夠高效地操作集合資料結構。