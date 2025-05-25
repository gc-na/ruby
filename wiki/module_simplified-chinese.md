<!--
Meta Description: # Ruby 模块(Module)详解 ## 概述 Ruby 中的模块（Module）是一种可以包含方法和常量的集合，用于组织代码和实现命名空间。模块无法实例化，但可以包含方法、类和常量，并可以通过混入（mix-in）的方式被类使用。 ## 文档 ### 目的 模块主要用于： - 代码重用：通过将共...
Meta Keywords: ruby, end, module, include, hello
-->

# Ruby 模块(Module)详解

## 概述
Ruby 中的模块（Module）是一种可以包含方法和常量的集合，用于组织代码和实现命名空间。模块无法实例化，但可以包含方法、类和常量，并可以通过混入（mix-in）的方式被类使用。

## 文档
### 目的
模块主要用于：
- 代码重用：通过将共享的功能放入模块中，多个类可以共享这些方法。
- 命名空间：避免命名冲突，通过模块划分不同的功能区。

### 用法
在 Ruby 中定义模块的基本语法如下：
```ruby
module ModuleName
  # 方法或常量定义
end
```

要在类中使用模块的方法，可以使用 `include` 或 `extend` 关键字：
- `include`：将模块的方法作为实例方法引入类中。
- `extend`：将模块的方法作为类方法引入类中。

### 详细说明
- 模块不能被实例化。
- 模块可以包含其他模块。
- 常量在模块中定义后，可以通过 `ModuleName::ConstantName` 的方式访问。
- 模块中定义的方法在类中可以直接使用，无需前缀。

## 示例
```ruby
module Greeting
  def hello
    puts "Hello!"
  end
end

class Person
  include Greeting
end

person = Person.new
person.hello  # 输出 "Hello!"
```

### 使用模块作为命名空间
```ruby
module MathOperations
  PI = 3.14

  def self.area_of_circle(radius)
    PI * radius ** 2
  end
end

puts MathOperations::PI  # 输出 3.14
puts MathOperations.area_of_circle(5)  # 输出 78.5
```

## 解释
- **常见陷阱**：在使用 `include` 时，如果模块中的方法与类中已有的方法同名，类中的方法会覆盖模块中的方法。
- **混入（Mix-in）注意事项**：当多个模块混入同一类时，方法的查找顺序遵循“最后包含的模块优先”的原则。
- **命名空间**：使用模块作为命名空间时，如果需要访问模块中的常量或方法，务必使用模块名作为前缀。

## 一句话总结
Ruby 中的模块用于组织代码、实现代码重用和避免命名冲突，但不能被实例化。