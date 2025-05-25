<!--
Meta Description: # Understanding 'rescue' in Ruby: Exception Handling Made Easy ## Synopsis The `rescue` keyword in Ruby is used to handle exceptions gracefully, allow...
Meta Keywords: rescue, ruby, exception, result, error
-->

# Understanding 'rescue' in Ruby: Exception Handling Made Easy

## Synopsis
The `rescue` keyword in Ruby is used to handle exceptions gracefully, allowing developers to manage errors and maintain control over program flow without crashing the application.

## Documentation
In Ruby, `rescue` is a part of the exception handling mechanism that provides a way to catch and respond to exceptions that may occur during the execution of code. When an error is raised, the normal flow of execution is interrupted; however, with `rescue`, developers can define specific actions to take when an exception occurs.

### Purpose
The primary purpose of `rescue` is to prevent program crashes caused by unhandled exceptions. By wrapping potentially error-prone code within a `begin...rescue` block, developers can ensure that their applications handle errors in a controlled manner.

### Usage
The basic syntax for using `rescue` is as follows:

```ruby
begin
  # Code that may raise an exception
rescue SomeExceptionClass => e
  # Code to handle the exception
end
```

You can also rescue from multiple exceptions or handle all exceptions using a generic rescue clause:

```ruby
begin
  # Code that may raise an exception
rescue SpecificError => e
  # Handle specific error
rescue AnotherError => e
  # Handle another specific error
rescue => e
  # Handle any other error
end
```

### Inline Rescue
Ruby also allows for inline rescue statements, which can be useful for simple error handling:

```ruby
result = some_risky_operation rescue default_value
```

This will assign `default_value` to `result` if `some_risky_operation` raises an exception.

## Examples

### Basic Example
```ruby
begin
  puts "Enter a number:"
  number = gets.chomp.to_i
  result = 10 / number
  puts "Result: #{result}"
rescue ZeroDivisionError => e
  puts "Error: Cannot divide by zero."
end
```

### Handling Multiple Exceptions
```ruby
begin
  puts "Enter a number:"
  number = gets.chomp
  result = 10 / number.to_i
  puts "Result: #{result}"
rescue ZeroDivisionError => e
  puts "Error: Division by zero is not allowed."
rescue ArgumentError => e
  puts "Error: Invalid input. Please enter a valid number."
end
```

### Inline Rescue Example
```ruby
result = 10 / (gets.chomp.to_i rescue 1)
puts "Result: #{result}"  # Defaults to dividing by 1 if input is invalid
```

## Explanation
While the `rescue` keyword is powerful, there are some common pitfalls to be aware of:

1. **Rescuing Too Broadly**: Using a generic `rescue` can make debugging difficult as it catches all exceptions, including those you may not want to handle. Always aim to rescue specific exceptions if possible.

2. **Not Raising Exceptions**: After handling an exception, if you need to propagate it further, use `raise` to re-raise the current exception.

3. **Ensure Clean-up Code**: If you need to ensure that some code runs regardless of whether an exception was raised (like closing files), use an `ensure` block in conjunction with your `rescue`.

4. **Avoid Nested Rescues**: Nested `begin...rescue` blocks can lead to code that is hard to read and maintain. Instead, consider refactoring to keep your error handling clear and concise.

## One Line Summary
The `rescue` keyword in Ruby simplifies exception handling, allowing developers to manage errors gracefully and maintain application stability.