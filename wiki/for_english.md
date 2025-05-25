<!--
Meta Description: # The Ruby `for` Loop: A Comprehensive Guide ## Synopsis The `for` loop in Ruby is a control structure that allows developers to iterate over a collec...
Meta Keywords: ruby, loop, each, over, collection
-->

# The Ruby `for` Loop: A Comprehensive Guide

## Synopsis
The `for` loop in Ruby is a control structure that allows developers to iterate over a collection of elements, such as arrays or ranges, executing a block of code for each element.

## Documentation
The `for` loop in Ruby provides a simple syntax for iterating through a collection. It is particularly useful when you need to process each element of an enumerable object sequentially.

### Purpose
The primary purpose of the `for` loop is to enable easy and efficient iteration over collections, such as arrays and ranges, without the need for manual index management.

### Usage
The syntax for a `for` loop in Ruby is as follows:

```ruby
for variable in collection do
  # code to be executed for each element
end
```

Where `variable` is a placeholder for the current element of the `collection`, which can be an array, a range, or any object that includes the `each` method.

### Details
- The `for` loop can iterate over various collections, including arrays, hashes (through their keys or values), and ranges.
- The loop will execute the block of code for each element until all elements in the collection have been processed.

## Examples
Here are some basic usage examples of the `for` loop in Ruby:

### Example 1: Iterating Over an Array
```ruby
fruits = ["apple", "banana", "cherry"]

for fruit in fruits do
  puts fruit
end
```
**Output:**
```
apple
banana
cherry
```

### Example 2: Iterating Over a Range
```ruby
for number in 1..5 do
  puts number
end
```
**Output:**
```
1
2
3
4
5
```

### Example 3: Iterating Over a Hash
```ruby
person = {name: "Alice", age: 30, city: "New York"}

for key, value in person do
  puts "#{key}: #{value}"
end
```
**Output:**
```
name: Alice
age: 30
city: New York
```

## Explanation
### Common Pitfalls
- **Scope of Variables:** The variable used in the `for` loop is accessible outside the loop, which can lead to unexpected behavior if the variable is reused elsewhere in the code.
- **Performance Considerations:** Although the `for` loop is straightforward, it may not be as performant as other iteration methods like `each` when dealing with large collections due to its syntax and context.

### Gotchas
- The `for` loop is often less idiomatic in Ruby compared to methods like `each`, `map`, or `select`, which are more commonly used in Ruby codebases.
- Nested `for` loops can lead to complicated and hard-to-read code. It's generally advisable to use more idiomatic Ruby methods for such cases.

## One Line Summary
The `for` loop in Ruby allows for straightforward iteration over collections, executing a block of code for each element in the collection.