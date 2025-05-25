<!--
Meta Description: # Ruby中的「rescue」關鍵字：異常處理的利器 ## 概要 在Ruby編程語言中，「rescue」關鍵字用於捕獲和處理異常，確保程式在遇到錯誤時不會崩潰，並允許開發者進行適當的錯誤處理。 ## 文檔 ### 目的 「rescue」是Ruby的一個異常處理機制，讓開發者能夠針對可能發生的錯誤進...
Meta Keywords: rescue, puts, begin, end, message
-->

# Ruby中的「rescue」關鍵字：異常處理的利器

## 概要
在Ruby編程語言中，「rescue」關鍵字用於捕獲和處理異常，確保程式在遇到錯誤時不會崩潰，並允許開發者進行適當的錯誤處理。

## 文檔
### 目的
「rescue」是Ruby的一個異常處理機制，讓開發者能夠針對可能發生的錯誤進行處理，從而提高程式的穩定性和可預測性。

### 用法
「rescue」通常與`begin`和`end`關鍵字一起使用，形成一個異常處理塊。若在`begin`塊中發生異常，控制流會自動跳轉至`rescue`塊進行處理。

```ruby
begin
  # 可能引發異常的代碼
  risky_operation()
rescue StandardError => e
  # 錯誤處理代碼
  puts "發生了錯誤: #{e.message}"
end
```

### 詳細說明
- `begin`塊中包含可能會引發異常的代碼。
- `rescue`允許捕獲特定類型的異常（如`StandardError`）。
- 可以使用多個`rescue`來捕獲不同類型的異常。
- 也可以使用`ensure`關鍵字定義無論是否發生異常都會執行的代碼。

## 範例
```ruby
# 示例1: 基本異常處理
begin
  puts 10 / 0
rescue ZeroDivisionError => e
  puts "除以零錯誤: #{e.message}"
end

# 示例2: 捕獲多種異常
begin
  puts "開始操作..."
  puts 10 / 0
  puts "這行不會執行"
rescue ZeroDivisionError => e
  puts "除以零錯誤: #{e.message}"
rescue StandardError => e
  puts "其他錯誤: #{e.message}"
end
```

## 解釋
- **常見坑洞**：使用不當的`rescue`可能會隱藏程式中的錯誤，導致難以排查問題。建議僅捕獲必要的異常。
- **不捕獲從`SystemExit`或`Interrupt`派生的異常**：這些異常通常用於終止程式，不應被捕獲。
- **多層嵌套的`begin-rescue`**：嵌套使用時需要特別注意作用域和捕獲的異常類型。

## 一句總結
「rescue」關鍵字在Ruby中是一種強大的異常處理機制，幫助開發者有效管理程式中的錯誤。