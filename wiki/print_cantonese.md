<!--
Meta Description: # Ruby 嘅 "print" 命令：完整指南 ## 概述 `print` 係 Ruby 中用來輸出資料嘅一個基本命令，佢唔會自動換行，適合用於需要連續顯示內容嘅場景。 ## 文檔 `print` 命令嘅主要目的是將資料輸出到標準輸出（通常係螢幕）。同時，佢唔會喺每次輸出後自動換行，這意味著所有輸...
Meta Keywords: print, ruby, name, age, line
-->

# Ruby 嘅 "print" 命令：完整指南

## 概述
`print` 係 Ruby 中用來輸出資料嘅一個基本命令，佢唔會自動換行，適合用於需要連續顯示內容嘅場景。

## 文檔
`print` 命令嘅主要目的是將資料輸出到標準輸出（通常係螢幕）。同時，佢唔會喺每次輸出後自動換行，這意味著所有輸出會連續顯示在同一行上。

### 用法
```ruby
print(obj)
```
- `obj`：可以係任何 Ruby 對象，例如字串、數字、數組等。`print` 會將對象轉換成字串並輸出。

### 詳細說明
- `print` 只負責輸出資料，並唔會返回任何值。
- 若要輸出後換行，應使用 `puts` 命令。
- `print` 會將多個輸出連接在一行上，除非明確添加換行符號。

## 示例
### 基本用法
```ruby
print "Hello, "
print "World!"
```
輸出結果：
```
Hello, World!
```

### 輸出變量
```ruby
name = "Alice"
age = 30
print "Name: #{name}, Age: #{age}"
```
輸出結果：
```
Name: Alice, Age: 30
```

### 使用換行符
```ruby
print "This is on the first line.\n"
print "This is on the second line."
```
輸出結果：
```
This is on the first line.
This is on the second line.
```

## 解釋
- **常見陷阱**：初學者可能會混淆 `print` 與 `puts`。`puts` 會自動在每次輸出後加上換行符，而 `print` 則唔會。
- **額外註解**：若需要在同一行上顯示多個資料，可以重複使用 `print`。但如果需要格式化輸出，考慮使用字串插值或者格式化函數。

## 一句總結
`print` 係 Ruby 中用來將資料輸出到標準輸出但唔自動換行嘅命令。