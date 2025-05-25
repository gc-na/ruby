<!--
Meta Description: # Understanding "super" in Ruby: A Guide to Method Inheritance and Overriding ## Synopsis The `super` keyword in Ruby allows a method to call the same...
Meta Keywords: method, super, superclass, arguments, child
-->

# Understanding "super" in Ruby: A Guide to Method Inheritance and Overriding

## Synopsis
The `super` keyword in Ruby allows a method to call the same method from its superclass, facilitating method inheritance and providing a powerful mechanism for extending and modifying behavior in object-oriented programming.

## Documentation
In Ruby, `super` is used within a method to invoke the same method defined in its superclass. This feature is essential in object-oriented programming as it enables subclasses to enhance or modify behaviors inherited from parent classes, maintaining a connection to the original implementation.

### Purpose
- To call a method in the superclass that has been overridden in the subclass.
- To pass arguments from the subclass method to the superclass method if desired.

### Usage
The `super` keyword can be used in two primary ways:
1. **Without Arguments**: Calls the superclass method with the same arguments that were passed to the subclass method.
2. **With Arguments**: Explicitly passes specified arguments to the superclass method.

### Syntax
```ruby
super          # Calls the superclass method with the same parameters.
super(arg1)   # Calls the superclass method with specified arguments.
```

## Examples

### Basic Example
```ruby
class Parent
  def greet
    puts "Hello from Parent"
  end
end

class Child < Parent
  def greet
    super  # Calls Parent's greet method
    puts "Hello from Child"
  end
end

child = Child.new
child.greet
```
**Output:**
```
Hello from Parent
Hello from Child
```

### Example with Arguments
```ruby
class Parent
  def greet(name)
    puts "Hello, #{name} from Parent"
  end
end

class Child < Parent
  def greet(name)
    super(name)  # Passes name to Parent's greet method
    puts "Hello, #{name} from Child"
  end
end

child = Child.new
child.greet("Alice")
```
**Output:**
```
Hello, Alice from Parent
Hello, Alice from Child
```

## Explanation
### Common Pitfalls
- **Omitting `super`**: If a subclass method does not call `super`, it completely overrides the superclass method, potentially losing essential functionality.
- **Argument Mismatch**: When using `super` with arguments, ensure that the superclass method accepts the parameters being passed. Mismatched arguments can lead to runtime errors.
- **Using `super()`**: Calling `super()` without parentheses will pass no arguments to the superclass method, while `super` (without parentheses) passes all arguments. This subtlety can lead to confusion.

### Additional Notes
- If a method in a subclass calls `super` without any arguments, it will automatically forward all the arguments received by the subclass method to the superclass method.
- Using `super` is an effective way to build on existing functionality, maintaining clean and manageable code through inheritance.

## One Line Summary
The `super` keyword in Ruby enables method overriding by allowing subclasses to invoke the corresponding method in their superclass, facilitating enhanced functionality and behavior modification.