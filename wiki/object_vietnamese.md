<!--
Meta Description: # Đối Tượng trong Ruby: Khám Phá Cấu Trúc Cơ Bản và Tính Năng ## Tóm Tắt Trong Ruby, "Đối Tượng" là một khái niệm cốt lõi trong lập trình hướng đối tư...
Meta Keywords: đối, tượng, một, trong, lớp
-->

# Đối Tượng trong Ruby: Khám Phá Cấu Trúc Cơ Bản và Tính Năng

## Tóm Tắt
Trong Ruby, "Đối Tượng" là một khái niệm cốt lõi trong lập trình hướng đối tượng, cho phép lập trình viên tạo ra các thực thể với thuộc tính và hành vi riêng biệt.

## Tài Liệu
### Mục Đích
Đối tượng trong Ruby đại diện cho một thực thể trong thế giới thực, với các thuộc tính (biến) và phương thức (hàm) để thực hiện các hành động. Ruby là một ngôn ngữ lập trình hoàn toàn hướng đối tượng, điều này có nghĩa rằng mọi thứ trong Ruby đều là đối tượng, kể cả các kiểu dữ liệu cơ bản như số và chuỗi.

### Cách Sử Dụng
Để tạo một đối tượng trong Ruby, trước tiên bạn cần định nghĩa một lớp (class). Một lớp là một bản thiết kế cho các đối tượng. Dưới đây là cú pháp cơ bản để tạo một lớp và sau đó khởi tạo một đối tượng từ lớp đó:

```ruby
class Dog
  def bark
    "Woof!"
  end
end

my_dog = Dog.new
puts my_dog.bark  # Kết quả: "Woof!"
```

### Chi Tiết
- **Khởi Tạo Đối Tượng**: Để tạo một đối tượng từ một lớp, bạn sử dụng phương thức `new`. Ví dụ, `Dog.new` tạo ra một đối tượng `Dog`.
- **Phương Thức**: Các phương thức trong lớp định nghĩa hành vi của đối tượng. Bạn có thể gọi phương thức bằng cách sử dụng dấu chấm (`.`).
- **Thuộc Tính**: Để lưu trữ thông tin về đối tượng, bạn có thể định nghĩa các thuộc tính bên trong lớp. Sử dụng `attr_accessor`, `attr_reader`, hoặc `attr_writer` để tạo thuộc tính dễ dàng hơn.

## Ví Dụ
### Ví dụ 1: Tạo đối tượng đơn giản
```ruby
class Car
  attr_accessor :color
  
  def initialize(color)
    @color = color
  end
  
  def honk
    "Beep!"
  end
end

my_car = Car.new("red")
puts my_car.color  # Kết quả: "red"
puts my_car.honk   # Kết quả: "Beep!"
```

### Ví dụ 2: Đối tượng với thuộc tính và phương thức
```ruby
class Person
  attr_accessor :name, :age

  def initialize(name, age)
    @name = name
    @age = age
  end

  def introduce
    "Hello, my name is #{@name} and I'm #{@age} years old."
  end
end

person = Person.new("Alice", 30)
puts person.introduce  # Kết quả: "Hello, my name is Alice and I'm 30 years old."
```

## Giải Thích
- **Nhầm Lẫn với Lớp**: Nhiều người mới bắt đầu có thể nhầm lẫn giữa lớp và đối tượng. Lớp là bản thiết kế, trong khi đối tượng là một thực thể cụ thể được tạo ra từ lớp đó.
- **Biến Instance**: Biến bắt đầu bằng `@` là biến instance, chúng chỉ có thể được truy cập từ các phương thức trong cùng một đối tượng. Điều này có thể gây ra nhầm lẫn nếu không được sử dụng đúng cách.
- **Các Phương Thức Khác**: Ruby cung cấp nhiều phương thức tích hợp sẵn để làm việc với đối tượng như `self`, `super`, và `initialize`.

## Tóm Tắt Một Câu
Trong Ruby, đối tượng là một thực thể của lớp, cho phép lập trình viên tạo ra các thực thể với thuộc tính và hành vi riêng biệt trong lập trình hướng đối tượng.