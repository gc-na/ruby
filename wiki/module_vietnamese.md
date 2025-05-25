<!--
Meta Description: # Module trong Ruby: Định nghĩa, Cách sử dụng và Ví dụ ## Tóm tắt Module trong Ruby là một cách để nhóm các phương thức, hằng số và các biến trong cùn...
Meta Keywords: module, dụng, phương, thức, trong
-->

# Module trong Ruby: Định nghĩa, Cách sử dụng và Ví dụ

## Tóm tắt
Module trong Ruby là một cách để nhóm các phương thức, hằng số và các biến trong cùng một không gian tên, cho phép tái sử dụng mã và tổ chức cấu trúc ứng dụng một cách hiệu quả.

## Tài liệu
Module trong Ruby được sử dụng để nhóm các phương thức và hằng số, giúp tổ chức mã nguồn và tránh xung đột tên. Module không thể được khởi tạo giống như lớp (class), nhưng nó có thể được sử dụng để bao gồm (include) hoặc mở rộng (extend) vào các lớp khác. Điều này cho phép các phương thức trong module có thể được gọi như một phần của lớp mà nó bao gồm.

### Mục đích
- Tổ chức mã nguồn và tăng tính tái sử dụng.
- Cung cấp không gian tên để tránh xung đột giữa các phương thức và hằng số.
- Cho phép chia sẻ phương thức giữa các lớp mà không cần kế thừa.

### Cách sử dụng
Để định nghĩa một module, bạn sử dụng từ khóa `module`, và để sử dụng module trong lớp, bạn sử dụng từ khóa `include` hoặc `extend`.

```ruby
module MyModule
  def greet
    puts "Hello from MyModule!"
  end
end

class MyClass
  include MyModule
end

obj = MyClass.new
obj.greet  # Kết quả: Hello from MyModule!
```

## Ví dụ
### Ví dụ 1: Sử dụng Module để bao gồm phương thức
```ruby
module MathHelper
  def add(a, b)
    a + b
  end
end

class Calculator
  include MathHelper
end

calc = Calculator.new
puts calc.add(5, 3)  # Kết quả: 8
```

### Ví dụ 2: Sử dụng Module để mở rộng phương thức
```ruby
module Greeting
  def self.say_hello
    puts "Hello!"
  end
end

Greeting.say_hello  # Kết quả: Hello!
```

## Giải thích
Khi sử dụng module, có một số điểm cần lưu ý:
- Module không thể được khởi tạo giống như lớp. Bạn không thể tạo đối tượng từ module.
- Phương thức trong module có thể được gọi từ các lớp đã bao gồm chúng.
- Khi sử dụng `include`, các phương thức trong module sẽ được thêm vào không gian tên của lớp, trong khi `extend` sẽ thêm phương thức như một phương thức lớp.

Một số lỗi phổ biến bao gồm việc quên sử dụng `include` hoặc `extend`, dẫn đến việc không thể gọi phương thức trong module.

## Tóm tắt một câu
Module trong Ruby là công cụ mạnh mẽ để tổ chức mã nguồn, cho phép tái sử dụng và chia sẻ phương thức giữa các lớp mà không cần kế thừa.