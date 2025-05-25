<!--
Meta Description: # Ruby Dir 指令：操作目錄的強大工具 ## 概述 在 Ruby 中，`Dir` 是一個內建的類別，主要用來操作和管理檔案系統中的目錄。它提供了多種方法來創建、刪除、列出目錄內容以及更改當前工作目錄。 ## 文檔 `Dir` 類別提供了一系列的方法來處理目錄。它的主要用途包括： - **列出...
Meta Keywords: dir, path, ruby, rmdir, entries
-->

# Ruby Dir 指令：操作目錄的強大工具

## 概述
在 Ruby 中，`Dir` 是一個內建的類別，主要用來操作和管理檔案系統中的目錄。它提供了多種方法來創建、刪除、列出目錄內容以及更改當前工作目錄。

## 文檔
`Dir` 類別提供了一系列的方法來處理目錄。它的主要用途包括：

- **列出目錄內容**：使用 `Dir.entries` 或 `Dir.glob` 方法可以取得目錄中的檔案和子目錄。
- **創建和刪除目錄**：可以使用 `Dir.mkdir` 創建新目錄，使用 `Dir.rmdir` 刪除空目錄。
- **改變當前工作目錄**：`Dir.chdir` 方法可以更改當前的工作目錄。

### 主要方法
- `Dir.entries(path)`：返回指定目錄的所有檔案和目錄名稱。
- `Dir.glob(pattern)`：返回符合指定模式的檔案列表。
- `Dir.mkdir(path)`：創建一個新目錄。
- `Dir.rmdir(path)`：刪除指定的空目錄。
- `Dir.chdir(path)`：更改當前工作目錄。

## 範例
以下是一些使用 `Dir` 的基本範例：

```ruby
# 列出當前目錄的所有檔案和目錄
puts Dir.entries('.')

# 創建一個新目錄
Dir.mkdir('new_directory')

# 刪除空目錄
Dir.rmdir('new_directory')

# 更改當前工作目錄
Dir.chdir('/path/to/another_directory')
puts Dir.pwd # 印出當前工作目錄
```

## 解釋
使用 `Dir` 時，開發者需要注意以下幾點：

- 在刪除目錄時，`Dir.rmdir` 只允許刪除空目錄。若目錄內有檔案，將會引發錯誤。
- 使用 `Dir.glob` 時，請確保模式正確，以避免意外匹配不想要的檔案。
- 改變當前工作目錄後，若在同一程式中使用相對路徑，可能會導致無法找到檔案。

## 一句總結
`Dir` 類別是 Ruby 中操作檔案系統目錄的強大工具，能夠有效地管理和控制目錄的各種操作。