<!--
Meta Description: # Understanding `defined?` in Ruby: A Comprehensive Guide ## Synopsis The `defined?` keyword in Ruby is a powerful tool that checks if a given express...
Meta Keywords: defined, expression, ruby, nil, puts
-->

# Understanding `defined?` in Ruby: A Comprehensive Guide

## Synopsis
The `defined?` keyword in Ruby is a powerful tool that checks if a given expression or variable has been defined, returning `nil` or a description string.

## Documentation
### Purpose
The `defined?` keyword is used to determine whether a particular variable, method, or expression is defined in the current context. It helps prevent errors by allowing developers to check for the existence of variables or methods before attempting to use them.

### Usage
The syntax for using `defined?` is straightforward:

```ruby
defined?(expression)
```

- **expression**: This can be a variable, method, constant, or any other Ruby expression.

### Return Values
- Returns a string describing the type of the expression if it is defined (e.g., `"local-variable"`, `"method"`, or `"constant"`).
- Returns `nil` if the expression is not defined.

### Context
The `defined?` keyword can be particularly useful in scenarios involving dynamic code execution or when working with optional method definitions. It allows developers to write safer code by avoiding `NameError` or `NoMethodError`.

## Examples
Here are some basic usage examples of `defined?` in Ruby:

### Example 1: Checking a Local Variable
```ruby
x = 10
puts defined?(x)       # Output: "local-variable"
puts defined?(y)       # Output: nil
```

### Example 2: Checking a Method
```ruby
def my_method
  puts "Hello"
end

puts defined?(my_method)  # Output: "method"
puts defined?(undefined_method)  # Output: nil
```

### Example 3: Checking a Constant
```ruby
MY_CONSTANT = 100
puts defined?(MY_CONSTANT)  # Output: "constant"
puts defined?(UNDEFINED_CONSTANT)  # Output: nil
```

### Example 4: Using with Expressions
```ruby
puts defined?(1 + 1)   # Output: "expression"
puts defined?(nil)      # Output: "nil"
```

## Explanation
### Common Pitfalls
1. **Not Checking Scope**: Remember that `defined?` checks for the definition in the current scope. A variable defined in a different method or scope will return `nil`.
  
2. **Misinterpreting Return Values**: The return value of `defined?` can be a string or `nil`. Misunderstanding this can lead to incorrect condition checks.

3. **Using with Non-Identifiers**: Using `defined?` on literals (like numbers or strings) will return `"expression"` but may not provide useful information, as these literals are inherently defined.

### Additional Notes
- `defined?` can be used effectively in metaprogramming to check for the existence of methods or variables before invoking them.
- It is a compile-time check and does not execute the expression, which is why it is safe to use.

## One Line Summary
The `defined?` keyword in Ruby checks if a variable, method, or expression is defined, returning descriptive strings or `nil` based on its existence.