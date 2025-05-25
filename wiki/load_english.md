<!--
Meta Description: # Understanding `load` in Ruby: A Comprehensive Guide ## Synopsis The `load` method in Ruby is used to load and execute Ruby code from a specified fil...
Meta Keywords: load, file, ruby, will, hello
-->

# Understanding `load` in Ruby: A Comprehensive Guide

## Synopsis
The `load` method in Ruby is used to load and execute Ruby code from a specified file, allowing you to dynamically include and run scripts in your application during runtime.

## Documentation
### Purpose
The primary purpose of the `load` method is to read and execute the contents of a Ruby file. Unlike `require`, which ensures that a file is loaded only once, `load` will load the specified file every time it is called. This makes `load` suitable for scenarios where you need to reload changes made to a file without restarting the Ruby process.

### Usage
The syntax for the `load` method is as follows:

```ruby
load(file_name, wrap = false)
```

- `file_name`: A string representing the path to the Ruby file you wish to load. This can be a relative or absolute path.
- `wrap`: An optional boolean parameter (default is `false`) that, when set to `true`, will execute the loaded code in a new scope.

### Details
- **File Path**: If the `file_name` does not include a file extension, `.rb` will be appended automatically.
- **Error Handling**: If the specified file cannot be found or loaded, a `LoadError` will be raised.
- **Execution Context**: Code loaded via `load` has access to the current execution context, including local variables at the time of loading.

## Examples
### Basic Usage
Here is a simple example demonstrating the use of `load`:

1. **Creating a Ruby file (`hello.rb`)**:
   ```ruby
   puts "Hello, World!"
   ```

2. **Loading the file in another Ruby script**:
   ```ruby
   load 'hello.rb'
   ```

When you run the above script, it will output:
```
Hello, World!
```

### Reloading a File
If you modify `hello.rb` to:
```ruby
puts "Hello, Universe!"
```
and run the loading script again with `load`, it will display the new message:
```
Hello, Universe!
```

### Using the Wrap Parameter
To execute the loaded code in a new scope, you can use the `wrap` parameter:

```ruby
load 'hello.rb', true
```

This will run the code in a separate scope, making local variables in the loading script unavailable to the loaded file.

## Explanation
### Common Pitfalls
- **LoadError**: If the file path is incorrect or the file does not exist, you will encounter a `LoadError`. Always ensure the path is correct and the file is accessible.
- **Multiple Loads**: Keep in mind that using `load` repeatedly can lead to unexpected behavior if the loaded file changes state or has side effects since it will be executed anew each time.
- **Global State**: Be cautious about using `load` with files that modify global state or define classes/modules, as this can lead to conflicts or redundancy in definitions.

## One Line Summary
The `load` method in Ruby dynamically loads and executes code from a specified file each time it is called, allowing for real-time code updates during execution.