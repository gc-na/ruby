<!--
Meta Description: # Ruby Hash：全面了解 Ruby 中的雜湊表 ## 簡介 在 Ruby 編程語言中，Hash 是一種重要的資料結構，用於儲存鍵值對。Hash 使得資料操作變得靈活和高效，是許多 Ruby 程式的核心組件。 ## 文檔 ### 目的 Hash 在 Ruby 中用於儲存和操作數據，能夠使用鍵來...
Meta Keywords: hash, ruby, person, my_hash, name
-->

# Ruby Hash：全面了解 Ruby 中的雜湊表

## 簡介
在 Ruby 編程語言中，Hash 是一種重要的資料結構，用於儲存鍵值對。Hash 使得資料操作變得靈活和高效，是許多 Ruby 程式的核心組件。

## 文檔
### 目的
Hash 在 Ruby 中用於儲存和操作數據，能夠使用鍵來快速檢索對應的值。這使得 Hash 成為處理關聯數據的理想選擇。

### 用法
在 Ruby 中，可以使用大括號 `{}` 來創建 Hash，並用 `=>` 來指定鍵和值。例如：

```ruby
my_hash = { "name" => "Alice", "age" => 30 }
```

從 Ruby 1.9 起，還可以使用符號語法來創建 Hash：

```ruby
my_hash = { name: "Alice", age: 30 }
```

### 詳細說明
- **創建 Hash**：可以通過直接指定鍵值對來創建 Hash。也可以使用 `Hash.new` 方法創建空的 Hash。
- **存取值**：可以通過鍵來存取值，例如 `my_hash["name"]` 或 `my_hash[:name]`。
- **修改 Hash**：可以使用 `my_hash[:new_key] = "value"` 來新增或更新鍵值。
- **刪除鍵**：使用 `my_hash.delete(:key)` 可以刪除指定的鍵。

## 範例
### 創建和存取 Hash
```ruby
# 創建 Hash
person = { name: "Bob", age: 25 }

# 存取 Hash 值
puts person[:name]  # 輸出: Bob
puts person[:age]   # 輸出: 25
```

### 修改 Hash
```ruby
# 修改值
person[:age] = 26
puts person[:age]   # 輸出: 26

# 新增鍵值對
person[:city] = "Hong Kong"
puts person[:city]  # 輸出: Hong Kong
```

### 刪除鍵
```ruby
# 刪除鍵
person.delete(:city)
puts person[:city]  # 輸出: nil
```

## 解釋
在使用 Hash 時，開發者需要注意以下幾點：
- **鍵的唯一性**：Hash 中的鍵必須是唯一的，重複的鍵會覆蓋之前的值。
- **鍵的類型**：雖然 Hash 的鍵可以是任何資料類型，但使用符號作為鍵通常會更高效且更易於閱讀。
- **順序**：從 Ruby 1.9 開始，Hash 保留了插入的順序，這在處理有序數據時非常有用。

## 總結
Hash 是 Ruby 中一種靈活且強大的資料結構，適合用於儲存和操作關聯數據。