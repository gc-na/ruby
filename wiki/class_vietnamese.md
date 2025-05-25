<!--
Meta Description: # Lớp (Class) trong Ruby: Hướng Dẫn Chi Tiết và Ví Dụ ## Tóm tắt Lớp (Class) trong Ruby là một cấu trúc cơ bản cho phép người lập trình định nghĩa đối...
Meta Keywords: lớp, ruby, đối, tượng, name
-->

# Lớp (Class) trong Ruby: Hướng Dẫn Chi Tiết và Ví Dụ

## Tóm tắt
Lớp (Class) trong Ruby là một cấu trúc cơ bản cho phép người lập trình định nghĩa đối tượng và thuộc tính của chúng, giúp xây dựng các ứng dụng hướng đối tượng một cách dễ dàng và hiệu quả.

## Tài liệu
Trong Ruby, lớp (class) là một khái niệm quan trọng trong lập trình hướng đối tượng. Nó cho phép bạn tổ chức mã nguồn theo cách mô tả các đối tượng và hành vi của chúng. Lớp có thể chứa các phương thức (method) và thuộc tính (attribute), giúp tái sử dụng mã và duy trì tính tổ chức trong ứng dụng.

### Cách sử dụng lớp:
Để định nghĩa một lớp trong Ruby, sử dụng từ khóa `class`, theo sau là tên lớp. Tên lớp thường được viết hoa chữ cái đầu tiên của mỗi từ. Bên trong lớp, bạn có thể định nghĩa các thuộc tính và phương thức.

```ruby
class Dog
  attr_accessor :name, :breed

  def initialize(name, breed)
    @name = name
    @breed = breed
  end

  def bark
    puts "#{@name} says woof!"
  end
end
```

### Khởi tạo đối tượng:
Khi lớp đã được định nghĩa, bạn có thể tạo các đối tượng từ lớp đó bằng cách gọi phương thức `new`.

```ruby
my_dog = Dog.new("Buddy", "Golden Retriever")
my_dog.bark  # Kết quả: Buddy says woof!
```

## Ví dụ
Dưới đây là một vài ví dụ đơn giản về cách định nghĩa và sử dụng lớp trong Ruby:

### Ví dụ 1: Định nghĩa lớp Sinh viên

```ruby
class Student
  attr_accessor :name, :age

  def initialize(name, age)
    @name = name
    @age = age
  end

  def introduce
    puts "Hi, my name is #{@name} and I'm #{@age} years old."
  end
end

student1 = Student.new("Alice", 20)
student1.introduce  # Kết quả: Hi, my name is Alice and I'm 20 years old.
```

### Ví dụ 2: Kế thừa lớp

```ruby
class Animal
  def speak
    puts "Animal speaks!"
  end
end

class Cat < Animal
  def speak
    puts "Meow!"
  end
end

cat = Cat.new
cat.speak  # Kết quả: Meow!
```

## Giải thích
Khi làm việc với lớp trong Ruby, có một số điều cần lưu ý:
- **Kế thừa**: Ruby hỗ trợ kế thừa, cho phép một lớp kế thừa thuộc tính và phương thức của lớp cha. Đảm bảo rằng bạn hiểu cách thức hoạt động của việc kế thừa để tránh nhầm lẫn.
- **Biến instance**: Biến được định nghĩa với `@` trước tên biến là biến instance và chỉ có thể truy cập trong phạm vi của đối tượng.
- **Phương thức khởi tạo**: Phương thức `initialize` là phương thức đặc biệt được gọi khi một đối tượng mới được tạo ra. Đây là nơi lý tưởng để khởi tạo các thuộc tính của đối tượng.

### Lỗi thường gặp
- Quên sử dụng từ khóa `class` khi định nghĩa lớp.
- Không sử dụng `attr_accessor`, dẫn đến việc không thể truy cập các thuộc tính một cách dễ dàng.
- Quên gọi phương thức `new` để khởi tạo đối tượng từ lớp.

## Tóm tắt một câu
Lớp trong Ruby là một cấu trúc cho phép lập trình viên định nghĩa và tổ chức các đối tượng cùng thuộc tính và hành vi của chúng, hỗ trợ lập trình hướng đối tượng.