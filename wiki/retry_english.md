<!--
Meta Description: # Understanding the `retry` Keyword in Ruby: A Comprehensive Guide ## Synopsis The `retry` keyword in Ruby is used within exception handling blocks to...
Meta Keywords: retry, begin, block, rescue, exception
-->

# Understanding the `retry` Keyword in Ruby: A Comprehensive Guide

## Synopsis
The `retry` keyword in Ruby is used within exception handling blocks to re-execute a block of code when an exception occurs, allowing for graceful recovery from errors.

## Documentation
### Purpose
The `retry` keyword is primarily used within a `begin-rescue` block to reattempt the execution of code that previously raised an exception. This can be particularly useful in scenarios where transient errors may occur, such as network requests or file operations.

### Usage
To use `retry`, you must place it within a `rescue` clause that follows a `begin` block. When an exception is rescued, the code execution jumps to the point of the `retry`, effectively restarting the `begin` block.

### Syntax
```ruby
begin
  # Code that may raise an exception
rescue SomeSpecificError => e
  # Error handling logic
  retry # Re-attempt executing the 'begin' block
end
```

### Details
- The `retry` keyword can only be used inside a `rescue` clause.
- When `retry` is called, the entire `begin` block is executed again. This means that any code that precedes the `retry` inside the `begin` block will also be executed again.
- If a different exception occurs during the second execution, the same `rescue` clause will handle it again. To avoid infinite loops, it’s crucial to have a condition that eventually leads to a successful execution or a different outcome.

## Examples
### Basic Example
Here’s a simple example of using `retry` to handle a potential network request failure:

```ruby
require 'net/http'

def fetch_data(url)
  attempts = 0
  begin
    attempts += 1
    response = Net::HTTP.get_response(URI(url))
    puts response.body
  rescue SocketError => e
    puts "Network error: #{e.message}. Attempt ##{attempts}."
    retry if attempts < 3 # Retry up to 3 times
  end
end

fetch_data('http://example.com')
```

### Example with Different Exceptions
In this example, we use `retry` within a `rescue` clause to handle multiple types of exceptions:

```ruby
def read_file(file_path)
  begin
    content = File.read(file_path)
    puts content
  rescue Errno::ENOENT => e
    puts "File not found: #{e.message}. Trying again..."
    sleep(1) # Wait before retrying
    retry
  rescue Errno::EACCES => e
    puts "Permission denied: #{e.message}. Cannot proceed."
  end
end

read_file('non_existent_file.txt')
```

## Explanation
### Common Pitfalls
1. **Infinite Loop**: If the condition for retrying is not defined correctly, it may cause an infinite loop, continuously trying to execute the `begin` block without a successful outcome.
2. **State Loss**: Variables or states set prior to the retry may be reset, which can lead to unexpected results if the block contains significant state changes.
3. **Not Handling All Exceptions**: Using `retry` without careful consideration of which exceptions to catch can lead to unhandled exceptions that cause the program to crash.

### Additional Notes
- It’s important to limit the number of retries or to implement a backoff strategy to prevent overwhelming resources.
- `retry` can only be used in the context of the `begin-rescue` block; it cannot be used outside of this structure.
- Always ensure that your retry logic is straightforward and comprehensible to avoid adding unnecessary complexity to your code.

## One Line Summary
The `retry` keyword in Ruby allows you to re-execute a block of code within a `begin-rescue` construct upon encountering an exception, facilitating error recovery.