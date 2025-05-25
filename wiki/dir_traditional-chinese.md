<!--
Meta Description: # Ruby Dir 模組：檔案與目錄操作的強大工具 ## 簡介 `Dir` 是 Ruby 語言中的一個標準庫模組，提供了一組用於操作檔案系統目錄的功能。透過 `Dir`，開發者可以輕鬆地讀取目錄內容、創建或刪除目錄、以及進行其他有關檔案和目錄的操作。 ## 文件說明 `Dir` 模組的主要目的在於...
Meta Keywords: dir, ruby, path, puts, new_directory
-->

# Ruby Dir 模組：檔案與目錄操作的強大工具

## 簡介
`Dir` 是 Ruby 語言中的一個標準庫模組，提供了一組用於操作檔案系統目錄的功能。透過 `Dir`，開發者可以輕鬆地讀取目錄內容、創建或刪除目錄、以及進行其他有關檔案和目錄的操作。

## 文件說明
`Dir` 模組的主要目的在於簡化與檔案系統的互動。無論是需要列出目錄中的檔案、檢查某個目錄是否存在，還是創建新的目錄，`Dir` 都能提供相關的方法來實現這些功能。使用 `Dir` 可以讓 Ruby 開發者有效地管理和操作檔案結構。

### 主要用途
- 列出目錄中的檔案和子目錄
- 創建和刪除目錄
- 讀取目錄的當前工作路徑
- 變更當前工作目錄
- 檢查目錄是否存在

## 使用範例

### 列出目錄內容
```ruby
Dir.foreach('/path/to/directory') do |filename|
  puts filename
end
```

### 創建新目錄
```ruby
Dir.mkdir('/path/to/new_directory') unless Dir.exist?('/path/to/new_directory')
```

### 刪除目錄
```ruby
Dir.rmdir('/path/to/directory_to_remove') if Dir.exist?('/path/to/directory_to_remove')
```

### 獲取當前工作目錄
```ruby
current_directory = Dir.pwd
puts current_directory
```

### 變更當前工作目錄
```ruby
Dir.chdir('/path/to/new_directory')
puts Dir.pwd  # 顯示新的當前工作目錄
```

## 解釋
使用 `Dir` 模組時，開發者需注意以下幾點：
- 在刪除目錄之前，必須確保目錄是空的，否則會引發錯誤。
- 使用 `Dir.foreach` 方法時，會列出目錄中的所有檔案，包括 `.` 和 `..` 這兩個特殊目錄。
- 對於文件和目錄的路徑，請確保使用正確的格式，以避免出現找不到路徑的錯誤。
- 在使用 `Dir.chdir` 變更當前工作目錄後，後續的檔案操作將基於新的工作目錄進行。

## 總結
`Dir` 模組為 Ruby 開發者提供了一個直觀且強大的工具來操作檔案系統中的目錄，簡化了相關操作的過程。