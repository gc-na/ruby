<!--
Meta Description: # Ruby中的defined?关键字：用法与示例 ## 概述 `defined?`是Ruby中的一个特殊关键字，用于检查一个变量、方法、常量或表达式是否已定义。它返回一个字符串，指示所检查的对象的类型，或者在未定义的情况下返回`nil`。 ## 文档 ### 目的 `defined?`的主要目的是...
Meta Keywords: defined, nil, puts, ruby, expression
-->

# Ruby中的defined?关键字：用法与示例

## 概述
`defined?`是Ruby中的一个特殊关键字，用于检查一个变量、方法、常量或表达式是否已定义。它返回一个字符串，指示所检查的对象的类型，或者在未定义的情况下返回`nil`。

## 文档
### 目的
`defined?`的主要目的是帮助开发者在运行时确认某个对象是否存在，以避免未定义的错误。

### 用法
`defined?`的基本语法如下：

```ruby
defined?(expression)
```

- **expression**：可以是变量、方法、常量或其他Ruby表达式。

### 返回值
- 如果表达式已定义，`defined?`返回一个描述性的字符串。
- 如果表达式未定义，返回`nil`。

### 细节
- `defined?`与`nil?`不同，因为`defined?`不抛出错误，而是安全地检查对象是否存在。
- 它在条件语句中常被使用，以确保代码的健壮性。

## 示例
以下是`defined?`的基本用法示例：

```ruby
# 定义一个变量
x = 10

# 检查变量是否定义
puts defined?(x)        # 输出 "local-variable"
puts defined?(y)        # 输出 nil，因为y未定义

# 检查方法是否定义
def my_method; end
puts defined?(my_method) # 输出 "method"

# 检查常量是否定义
MyConstant = 100
puts defined?(MyConstant) # 输出 "constant"
```

## 解释
### 常见陷阱
- **局部变量与全局变量**：在不同的作用域中，变量的定义可能会有所不同，使用`defined?`时需要注意作用域。
- **方法和块**：在使用`defined?`检查方法时，确保方法在调用之前已定义。

### 注意事项
- `defined?`关键字不仅可以用于变量，还可以用于方法、常量以及其他表达式。
- 在使用时，确保表达式的上下文是清晰的，以避免误解返回值。

## 一句话总结
`defined?`是Ruby中的一个关键字，用于检查对象是否已定义，返回相应的类型描述或`nil`。