<!--
Meta Description: # Ruby 的 until 关键字详解：用法与示例 ## 概述 在 Ruby 编程语言中，`until` 是一个控制流结构，用于在特定条件为假时执行代码块。它与 `while` 关键字相对，`until` 语句在条件为 false 时运行，而当条件为 true 时停止执行。 ## 文档 ### 目...
Meta Keywords: until, number, ruby, true, end
-->

# Ruby 的 until 关键字详解：用法与示例

## 概述
在 Ruby 编程语言中，`until` 是一个控制流结构，用于在特定条件为假时执行代码块。它与 `while` 关键字相对，`until` 语句在条件为 false 时运行，而当条件为 true 时停止执行。

## 文档
### 目的
`until` 关键字用于创建一个循环，只有在给定条件为 false 时，才会持续执行代码块。这对于那些希望在某个条件未满足时重复执行某些操作的场景特别有用。

### 用法
`until` 的基本语法如下：

```ruby
until condition do
  # 执行的代码块
end
```

或者可以使用更简洁的形式：

```ruby
until condition
  # 执行的代码块
end
```

在上述语法中，`condition` 是一个表达式，当它的值为 true 时，循环将终止。

### 细节
- `until` 可以与 `break` 语句结合使用，以提前终止循环。
- 可以在 `until` 循环中使用多种数据类型进行条件判断，包括布尔值、数字、字符串等。
- 使用 `unless` 关键字可以实现与 `until` 相似的效果，但语义上是相反的。

## 示例
### 基本示例
以下是一个简单的 `until` 循环示例，该示例会打印数字，直到数字大于或等于 5：

```ruby
number = 0
until number >= 5 do
  puts number
  number += 1
end
```

### 使用 break 语句
以下示例展示了如何在 `until` 循环中使用 `break`：

```ruby
number = 0
until number >= 10 do
  puts number
  number += 1
  break if number == 5 # 当 number 等于 5 时退出循环
end
```

## 解释
使用 `until` 关键字时，开发者需要注意以下几点：
- 确保条件能够在某个时刻变为 true，以避免创建无限循环。
- 在某些情况下，使用 `while` 可能会更加直观，开发者应根据具体情况选择使用 `until` 或 `while`。
- 理解 `until` 和 `unless` 之间的区别，以便更好地利用 Ruby 的控制流结构。

## 一句话总结
`until` 是 Ruby 中的一个控制流结构，用于在条件为 false 时重复执行代码块，直到条件变为 true。