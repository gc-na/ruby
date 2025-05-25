<!--
Meta Description: # Understanding TrueClass in Ruby: A Comprehensive Guide ## Synopsis TrueClass is a built-in Ruby class that represents the boolean value `true`. It i...
Meta Keywords: trueclass, true, ruby, boolean, puts
-->

# Understanding TrueClass in Ruby: A Comprehensive Guide

## Synopsis
TrueClass is a built-in Ruby class that represents the boolean value `true`. It is a fundamental part of the Ruby programming language, enabling developers to work with boolean logic effectively.

## Documentation
### Purpose
TrueClass is one of the two classes in Ruby that represent boolean values; the other being FalseClass. The primary purpose of TrueClass is to provide a way to express the truth value `true` in Ruby programs, which is essential for control flow, conditional statements, and logical operations.

### Usage
TrueClass instances can be used in various contexts, including:

- Conditional statements (`if`, `unless`, etc.)
- Boolean operations (e.g., `and`, `or`, `not`)
- Comparisons and assertions

In Ruby, `true` is an instance of TrueClass, and it behaves predictably when used in logical expressions.

### Details
- **Inheritance**: TrueClass is a subclass of Object, which means it inherits methods from Object and can be used as a base for other classes.
- **Methods**: TrueClass includes several methods, such as:
  - `&`: Bitwise AND
  - `|`: Bitwise OR
  - `^`: Bitwise XOR
  - `!`: Logical NOT
  - `to_s`: Converts the boolean to a string representation (`"true"`).

## Examples
Here are a few basic usage examples of TrueClass in Ruby:

### Example 1: Simple Conditional Statement
```ruby
is_active = true

if is_active
  puts "The system is active."
else
  puts "The system is inactive."
end
```

### Example 2: Logical Operations
```ruby
a = true
b = false

puts a && b  # Outputs: false
puts a || b  # Outputs: true
puts !a      # Outputs: false
```

### Example 3: Using TrueClass in an Array
```ruby
bool_array = [true, false, true]

bool_array.each do |bool|
  puts bool.class  # Outputs: TrueClass or FalseClass
end
```

## Explanation
While working with TrueClass, developers should be aware of certain common pitfalls:

- **Boolean Context**: Only `true` and `false` are considered boolean values in Ruby. Any other object is treated as truthy in conditional statements. For instance, `if 1` will evaluate to `true`, while `if 0` evaluates to `true` as well. This can sometimes lead to confusion if not carefully considered.
  
- **Method Override**: Since TrueClass inherits from Object, it is possible to override methods that may change its expected behavior. This is generally not recommended, as it can introduce unexpected results in conditional logic.

- **Immutability**: The value `true` is immutable, meaning it cannot be altered once created. This ensures consistency throughout a Ruby program.

## One Line Summary
TrueClass in Ruby represents the boolean value `true`, providing essential functionality for logical operations and control flow in programming.