<!--
Meta Description: # Understanding `undef` in Ruby: A Comprehensive Guide ## Synopsis The `undef` keyword in Ruby is used to remove method definitions from a class or mo...
Meta Keywords: undef, method, class, ruby, end
-->

# Understanding `undef` in Ruby: A Comprehensive Guide

## Synopsis
The `undef` keyword in Ruby is used to remove method definitions from a class or module, allowing developers to redefine or prevent the use of specific methods.

## Documentation
### Purpose
The primary purpose of `undef` is to provide a mechanism for dynamically altering the behavior of classes and modules in Ruby. By using `undef`, developers can prevent the invocation of methods that may not be appropriate for a given context or that need to be overridden in subclasses.

### Usage
The `undef` keyword can be used within class or module definitions to specify a list of methods to be undefined. Once a method is undefined, any attempt to call it will result in a `NoMethodError`.

#### Syntax
```ruby
undef method_name
```

You can also undefine multiple methods in a single statement:
```ruby
undef method1, method2, method3
```

### Details
- `undef` can only be used on methods that are already defined within the same class or module.
- The `undef` statement can be placed anywhere within a class or module definition but is typically used after method definitions.
- It does not affect instance variables or class variables, only methods.
- If a method is undefined, it cannot be called by instances of the class or module; however, it can still be called by subclasses unless specifically redefined.

## Examples
### Basic Example
```ruby
class Example
  def greet
    puts "Hello!"
  end

  undef greet
end

example = Example.new
# This will raise a NoMethodError
example.greet # => NoMethodError: undefined method `greet'
```

### Undefining Multiple Methods
```ruby
class Calculator
  def add(a, b)
    a + b
  end

  def subtract(a, b)
    a - b
  end

  undef add, subtract
end

calculator = Calculator.new
# Both will raise NoMethodError
calculator.add(5, 3)      # => NoMethodError: undefined method `add'
calculator.subtract(5, 3) # => NoMethodError: undefined method `subtract'
```

### Redefining After Undefining
```ruby
class Person
  def name
    "John Doe"
  end

  undef name
  
  def name
    "Jane Doe"
  end
end

person = Person.new
puts person.name # => "Jane Doe"
```

## Explanation
### Common Pitfalls
- Attempting to undefine a method that does not exist will not raise an error at the point of the `undef` statement, but attempting to call the method later will lead to a `NoMethodError`.
- If you undefine a method in a superclass, you cannot call it from an instance of a subclass unless it is redefined in the subclass.

### Gotchas
- Using `undef` can lead to confusion if not documented properly, as it alters the expected behavior of class instances.
- Developers should ensure that `undef` is used judiciously to maintain code readability and prevent unexpected behavior.

## One Line Summary
The `undef` keyword in Ruby allows developers to remove method definitions from classes or modules, preventing their use and enabling flexible method redefinition.