<!--
Meta Description: # Ruby中的load命令详解：动态加载Ruby文件 ## 概述 `load` 是 Ruby 编程语言中的一个重要命令，用于动态加载和执行指定的 Ruby 文件。与其他加载机制相比，`load` 命令每次都会重新加载文件，适用于需要频繁更新代码的场景。 ## 文档 ### 目的 `load` 命令...
Meta Keywords: load, ruby, wrap, hello, main
-->

# Ruby中的load命令详解：动态加载Ruby文件

## 概述
`load` 是 Ruby 编程语言中的一个重要命令，用于动态加载和执行指定的 Ruby 文件。与其他加载机制相比，`load` 命令每次都会重新加载文件，适用于需要频繁更新代码的场景。

## 文档
### 目的
`load` 命令的主要目的是从指定路径加载 Ruby 文件，并执行其中的代码。它在调试和开发过程中尤其有用，因为可以在不重启 Ruby 解释器的情况下，实时更新文件的内容。

### 用法
`load` 的基本语法如下：
```ruby
load(file, wrap = false)
```
- `file`：要加载的文件的路径，可以是相对路径或绝对路径。
- `wrap`：一个可选参数，默认为 `false`。如果设置为 `true`，则会在加载文件时将其放入一个新的作用域中。

### 细节
- 每次调用 `load` 都会重新读取并执行指定的文件，这意味着文件中的变量和方法会被重新定义。
- `load` 可以加载任意 Ruby 文件，不仅限于以 `.rb` 结尾的文件。
- 如果指定的文件不存在，`load` 将抛出 `LoadError` 异常。

## 示例
### 基本用法
以下是一个简单的示例，演示如何使用 `load` 命令加载并执行一个 Ruby 文件：
```ruby
# hello.rb
puts "Hello, World!"

# main.rb
load 'hello.rb'
```
运行 `main.rb` 将输出：
```
Hello, World!
```

### 使用 wrap 参数
如果需要在新的作用域中加载文件，可以使用 `wrap` 参数：
```ruby
# example.rb
$global_var = "I'm global"
local_var = "I'm local"

# main.rb
load 'example.rb', true
puts $global_var   # => "I'm global"
puts local_var     # => NameError: undefined local variable or method `local_var' for main:Object
```

## 说明
- **常见陷阱**：由于 `load` 在每次调用时都会重新加载文件，因此如果文件中定义了方法或类，可能会导致意外的覆盖或重新定义。要小心处理这种情况。
- **使用场景**：在开发过程中，当需要对代码进行频繁修改并希望立即看到效果时，`load` 是一个非常方便的工具。而在生产环境中，通常建议使用 `require` 或 `require_relative`，因为它们会缓存加载的文件，避免重复加载。

## 一句话总结
`load` 命令在 Ruby 中用于动态加载和执行指定的 Ruby 文件，每次调用都会重新执行文件中的内容。