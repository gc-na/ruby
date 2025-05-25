<!--
Meta Description: # Ruby 中的 `ensure`：確保代碼執行的關鍵字 ## 概述 在 Ruby 中，`ensure` 是一個關鍵字，用於確保某段代碼無論是否發生異常都會執行。這對於資源釋放和清理工作非常重要，例如關閉文件或釋放網絡連接。 ## 文檔 `ensure` 是 Ruby 的異常處理機制的一部分，通常...
Meta Keywords: ensure, ruby, rescue, file, begin
-->

# Ruby 中的 `ensure`：確保代碼執行的關鍵字

## 概述
在 Ruby 中，`ensure` 是一個關鍵字，用於確保某段代碼無論是否發生異常都會執行。這對於資源釋放和清理工作非常重要，例如關閉文件或釋放網絡連接。

## 文檔
`ensure` 是 Ruby 的異常處理機制的一部分，通常與 `begin` 和 `rescue` 搭配使用。當代碼塊內發生異常時，`ensure` 中的代碼將始終執行。這使得程序在處理異常時能保持穩定性和可靠性。

### 使用方法
```ruby
begin
  # 可能會發生異常的代碼
rescue SomeException => e
  # 處理異常的代碼
ensure
  # 無論是否發生異常，這段代碼都會被執行
end
```

### 詳細說明
- `begin`：開始一個異常處理的代碼塊。
- `rescue`：捕捉並處理異常。
- `ensure`：確保代碼塊內的代碼在完成後無論有無異常都會執行。

這對於確保重要的清理操作始終執行非常有用。即使在異常發生的情況下，`ensure` 中的代碼也會被執行，這樣可以防止資源洩漏。

## 範例
### 基本使用範例
```ruby
def read_file(file_name)
  file = File.open(file_name)
  # 讀取文件內容
  # 可能會發生異常
rescue Errno::ENOENT
  puts "文件不存在"
ensure
  file.close if file
  puts "文件已關閉"
end

read_file("不存在的文件.txt")
```

在這個例子中，即使文件不存在，`ensure` 中的 `file.close` 仍然會被執行，這樣可以避免資源洩漏。

## 解釋
- **常見陷阱**：如果在 `ensure` 塊中發生異常，這個異常會覆蓋之前的異常，因此在 `ensure` 中的代碼也應該小心處理。
- **注意事項**：`ensure` 是一個很好的工具，但不應該用來代替 `rescue`，而是作為異常處理的補充。

## 一句總結
`ensure` 使 Ruby 開發者能夠確保某段代碼在異常情況下仍然執行，從而保持程序的穩定性和資源的有效管理。