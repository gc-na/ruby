<!--
Meta Description: # Ruby中的“for”循环：用法与示例 ## 概述 在Ruby编程语言中，“for”循环是一种用于迭代集合（如数组或范围）的控制结构。它允许开发者在每次循环中执行指定的代码块，简化了重复任务的处理。 ## 文档 “for”循环的主要目的是提供一个简单的方式来遍历元素。其基本语法如下： ```ru...
Meta Keywords: end, each, ruby, collection, items
-->

# Ruby中的“for”循环：用法与示例

## 概述
在Ruby编程语言中，“for”循环是一种用于迭代集合（如数组或范围）的控制结构。它允许开发者在每次循环中执行指定的代码块，简化了重复任务的处理。

## 文档
“for”循环的主要目的是提供一个简单的方式来遍历元素。其基本语法如下：

```ruby
for variable in collection
  # 循环体
end
```

- **variable**：在每次迭代中代表当前元素的变量。
- **collection**：可以是数组、范围或任何实现了`each`方法的对象。

### 用法
1. **数组遍历**：
   使用“for”循环可以轻松遍历数组中的每个元素。

2. **范围遍历**：
   可以使用“for”循环遍历一定范围内的数字。

3. **自定义对象**：
   任何实现了`each`方法的对象都可以被“for”循环遍历。

## 示例
### 遍历数组
```ruby
fruits = ["苹果", "香蕉", "橙子"]
for fruit in fruits
  puts fruit
end
```

### 遍历范围
```ruby
for i in 1..5
  puts i
end
```

### 自定义对象遍历
```ruby
class MyCollection
  include Enumerable

  def initialize(items)
    @items = items
  end

  def each(&block)
    @items.each(&block)
  end
end

collection = MyCollection.new([10, 20, 30])
for item in collection
  puts item
end
```

## 说明
- **注意事项**：
  - “for”循环的作用域在循环体外是可见的，意味着在循环中定义的变量会泄露到外部。
  - 推荐在需要使用变量的作用域时小心使用“for”循环，可能会导致意外的结果。

- **性能**：
  - 虽然“for”循环在许多情况下是有效的，但在性能敏感的代码中，使用`each`方法或其他迭代方法可能会更合适。

## 一句话总结
Ruby中的“for”循环是一种简单的方式，用于迭代集合中的元素。