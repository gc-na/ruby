<!--
Meta Description: # Ruby 的 "rescue" 指令：錯誤處理的關鍵工具 ## 簡介 在 Ruby 中，`rescue` 是一個關鍵字，主要用於錯誤和異常處理。它讓開發者能夠捕捉執行時的錯誤，並進行相應的處理，從而提高程式的穩定性和健壯性。 ## 文件說明 ### 目的 `rescue` 用於捕獲和處理異常，使...
Meta Keywords: rescue, ruby, begin, end, puts
-->

# Ruby 的 "rescue" 指令：錯誤處理的關鍵工具

## 簡介
在 Ruby 中，`rescue` 是一個關鍵字，主要用於錯誤和異常處理。它讓開發者能夠捕捉執行時的錯誤，並進行相應的處理，從而提高程式的穩定性和健壯性。

## 文件說明
### 目的
`rescue` 用於捕獲和處理異常，使得程式在遇到錯誤時不至於崩潰。通過使用 `rescue`，開發者可以定義錯誤發生時的行為，進而自動處理錯誤情況。

### 用法
`rescue` 可以獨立使用，也可以與 `begin` 和 `end` 共同使用，形成一個完整的錯誤處理結構。基本語法如下：

```ruby
begin
  # 可能會引發錯誤的代碼
rescue 錯誤類型
  # 處理錯誤的代碼
end
```

如果不指定錯誤類型，`rescue` 將捕獲所有異常。

### 例子
以下是幾個使用 `rescue` 的基本示例：

1. 捕獲所有異常：
   ```ruby
   begin
     # 可能會引發錯誤的代碼
     result = 10 / 0
   rescue
     puts "發生了錯誤！"
   end
   ```

2. 捕獲特定異常：
   ```ruby
   begin
     # 嘗試打開不存在的文件
     file = File.open("不存在的文件.txt")
   rescue Errno::ENOENT
     puts "文件未找到！"
   end
   ```

3. 在 `rescue` 中使用 `else` 和 `ensure`：
   ```ruby
   begin
     result = 10 / 2
   rescue ZeroDivisionError
     puts "不能除以零！"
   else
     puts "計算成功，結果是 #{result}"
   ensure
     puts "這段代碼無論如何都會執行。"
   end
   ```

## 解釋
使用 `rescue` 時，開發者需要注意以下幾個常見的問題：

1. **捕獲範圍**：確保正確捕獲所需的異常類型，避免過度捕獲（例如，捕獲所有異常）。這可能導致錯誤被隱藏，讓調試變得困難。

2. **使用 `else` 和 `ensure`**：了解 `else` 和 `ensure` 的用法，可以讓錯誤處理更加靈活和完整。`else` 會在 `begin` 區塊無異常時執行，而 `ensure` 則始終執行。

3. **性能考量**：過多的錯誤捕獲可能影響性能，特別是在高頻率執行的代碼中。合理使用 `rescue` 可以減少性能損耗。

## 單行總結
Ruby 中的 `rescue` 是一個強大的工具，用於優雅地處理錯誤和異常，提升程式的穩定性。