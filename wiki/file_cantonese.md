<!--
Meta Description: # Ruby中的檔案操作：File 類別詳解 ## 概述 在Ruby中，`File` 類別用於檔案的讀取、寫入和管理。它提供了強大而靈活的功能，讓開發者能夠輕鬆地與檔案系統進行互動。 ## 文件說明 `File` 類別是Ruby標準庫的一部分，主要用於處理檔案的創建、修改、讀取和關閉。這個類別提供了...
Meta Keywords: file, puts, ruby, example, txt
-->

# Ruby中的檔案操作：File 類別詳解

## 概述
在Ruby中，`File` 類別用於檔案的讀取、寫入和管理。它提供了強大而靈活的功能，讓開發者能夠輕鬆地與檔案系統進行互動。

## 文件說明
`File` 類別是Ruby標準庫的一部分，主要用於處理檔案的創建、修改、讀取和關閉。這個類別提供了多種方法來進行檔案操作，讓開發者能夠方便地管理檔案內容。

### 主要功能
- **創建檔案**：使用 `File.new` 或 `File.open` 方法可以創建新檔案。
- **讀取檔案**：可使用 `File.read` 或 `File.foreach` 方法來讀取檔案內容。
- **寫入檔案**：透過 `File.write` 或 `File.open` 方法，可以將資料寫入檔案。
- **檔案屬性**：可使用方法如 `File.size`，`File.exist?` 來檢查檔案的存在性和大小。

## 使用範例
### 1. 創建與寫入檔案
```ruby
File.open("example.txt", "w") do |file|
  file.puts "這是第一行"
  file.puts "這是第二行"
end
```

### 2. 讀取檔案
```ruby
content = File.read("example.txt")
puts content
```

### 3. 檢查檔案存在性
```ruby
if File.exist?("example.txt")
  puts "檔案存在"
else
  puts "檔案不存在"
end
```

### 4. 逐行讀取檔案
```ruby
File.foreach("example.txt") do |line|
  puts line
end
```

## 解釋
在使用`File` 類別時，開發者可能會遇到一些常見問題：
- **檔案權限**：嘗試寫入檔案時，若無適當的權限，將會引發 `Errno::EACCES` 錯誤。
- **檔案不存在**：在讀取不存在的檔案時，會引發 `Errno::ENOENT` 錯誤。
- **資源管理**：確保檔案在使用後正確關閉，使用塊 (`do...end`) 是一個良好的習慣，因為這樣可以自動關閉檔案。

## 總結
`File` 類別為Ruby提供了一個強大的檔案操作工具，使開發者能夠高效地進行檔案的創建、讀取和管理。