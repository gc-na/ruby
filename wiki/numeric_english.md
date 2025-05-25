<!--
Meta Description: # Understanding Numeric in Ruby: A Comprehensive Guide ## Synopsis In Ruby, the `Numeric` class serves as the foundational superclass for all numeric ...
Meta Keywords: numeric, methods, ruby, class, types
-->

# Understanding Numeric in Ruby: A Comprehensive Guide

## Synopsis
In Ruby, the `Numeric` class serves as the foundational superclass for all numeric types, including integers, floats, and rational numbers, providing a consistent interface for mathematical operations and numeric manipulations.

## Documentation
### Purpose
The `Numeric` class in Ruby acts as a base class for all numeric types. It encapsulates the behavior of numbers and provides a common set of methods that can be utilized across different numeric types. This unification allows for seamless mathematical operations and comparisons.

### Usage
The `Numeric` class is not instantiated directly. Instead, it serves as a superclass for other numeric classes like `Integer`, `Float`, and `Rational`. As a user, you will typically interact with these subclasses, but understanding `Numeric` helps in grasping the available methods and functionalities.

### Details
- **Inheritance**: `Numeric` is an abstract class, meaning it is not intended to be used directly but provides a structure for its subclasses.
- **Key Methods**: 
  - Arithmetic operations: `+`, `-`, `*`, `/`, `%`
  - Comparison methods: `<`, `<=`, `>`, `>=`, `==`, `!=`
  - Conversion methods: `to_i`, `to_f`, `to_r`
  - Mathematical methods: `abs`, `ceil`, `floor`, `round`

### Numeric Hierarchy
The numeric hierarchy in Ruby is as follows:
```
Numeric
├── Integer
├── Float
└── Rational
```

## Examples
### Basic Usage
Here are some basic examples demonstrating the use of numeric types inherited from `Numeric`:

```ruby
# Integer Example
int_num = 10
puts int_num + 5          # Output: 15
puts int_num.to_f         # Output: 10.0

# Float Example
float_num = 3.14
puts float_num * 2        # Output: 6.28
puts float_num.round      # Output: 3

# Rational Example
require 'rational'
rational_num = Rational(1, 3)
puts rational_num + Rational(1, 6)  # Output: 1/2
```

## Explanation
### Common Pitfalls
- **Type Confusion**: Mixing different numeric types (e.g., integers with floats) can lead to unexpected results. Ruby automatically converts integers to floats when necessary, but being aware of this can help avoid precision issues.
- **Method Availability**: Certain methods may not be available for all subclasses of `Numeric`. For example, methods specific to `Float` will not be applicable to `Integer`.
- **Rounding Behavior**: When using rounding methods, be aware that Ruby uses "round half to even" by default, which may not align with typical rounding expectations.

### Additional Notes
- The `Numeric` class provides a rich set of methods that can be overridden in its subclasses, allowing for customized behavior specific to each numeric type.
- When performing operations on different numeric types, consider the precision and potential loss of information, particularly with floating-point numbers.

## One Line Summary
The `Numeric` class in Ruby serves as the abstract superclass for all numeric types, offering a unified interface for mathematical operations and numeric manipulations.