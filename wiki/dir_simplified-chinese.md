<!--
Meta Description: # Ruby Dir 模块详解：文件和目录操作的利器 ## 概述 Ruby 的 `Dir` 模块提供了一组用于处理文件和目录的功能，能够有效地创建、读取、和管理文件系统中的目录。无论是遍历目录、创建新目录还是删除目录，`Dir` 模块都提供了简单易用的接口。 ## 文档 `Dir` 模块的主要功能包...
Meta Keywords: dir, ruby, entry, puts, rmdir
-->

# Ruby Dir 模块详解：文件和目录操作的利器

## 概述
Ruby 的 `Dir` 模块提供了一组用于处理文件和目录的功能，能够有效地创建、读取、和管理文件系统中的目录。无论是遍历目录、创建新目录还是删除目录，`Dir` 模块都提供了简单易用的接口。

## 文档
`Dir` 模块的主要功能包括：

- **创建目录**：使用 `Dir.mkdir` 方法可以创建新目录。
- **删除目录**：使用 `Dir.rmdir` 方法可以删除空目录。
- **读取目录**：使用 `Dir.entries` 和 `Dir.foreach` 方法可以列出目录中的文件和子目录。
- **更改当前工作目录**：使用 `Dir.chdir` 方法可以更改当前工作目录。
- **获取当前工作目录**：使用 `Dir.pwd` 方法可以获取当前工作目录路径。

### 使用方法
在 Ruby 中使用 `Dir` 模块非常简单。以下是一些常用方法的基本语法：

- **创建目录**：
  ```ruby
  Dir.mkdir('新目录名')
  ```

- **删除目录**：
  ```ruby
  Dir.rmdir('目录名')
  ```

- **列出目录内容**：
  ```ruby
  entries = Dir.entries('目录路径')
  ```

- **遍历目录**：
  ```ruby
  Dir.foreach('目录路径') do |entry|
    puts entry
  end
  ```

- **更改当前工作目录**：
  ```ruby
  Dir.chdir('新工作目录')
  ```

- **获取当前工作目录**：
  ```ruby
  current_dir = Dir.pwd
  ```

## 示例
以下是一些基本的使用示例：

### 创建新目录
```ruby
Dir.mkdir('example_dir')
puts '目录创建成功'
```

### 删除空目录
```ruby
Dir.rmdir('example_dir')
puts '目录删除成功'
```

### 列出目录中的文件
```ruby
Dir.entries('.').each do |entry|
  puts entry
end
```

### 遍历目录
```ruby
Dir.foreach('.') do |entry|
  puts entry unless entry == '.' || entry == '..'
end
```

### 更改工作目录并获取当前目录
```ruby
Dir.chdir('/path/to/your/directory')
puts "当前工作目录是: #{Dir.pwd}"
```

## 说明
使用 `Dir` 模块时，有几个常见的注意事项：

- **空目录删除**：`Dir.rmdir` 只能删除空目录。如果目录中包含文件或其他子目录，试图删除将引发错误。
- **权限问题**：在某些情况下，创建或删除目录可能会因为权限问题而失败，确保程序运行时具有所需的文件系统权限。
- **路径问题**：使用相对路径时，确保当前工作目录正确，以避免出现 `FileNotFoundError`。

## 一句话总结
Ruby 的 `Dir` 模块提供了一系列简便的方法来操作文件和目录，使得文件系统的管理变得更加高效和直观。