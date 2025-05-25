<!--
Meta Description: # Từ Khóa "super" Trong Ruby: Hướng Dẫn Chi Tiết ## Tóm Tắt Từ khóa `super` trong Ruby được sử dụng để gọi phương thức cùng tên từ lớp cha trong ngữ c...
Meta Keywords: super, phương, thức, trong, dụng
-->

# Từ Khóa "super" Trong Ruby: Hướng Dẫn Chi Tiết

## Tóm Tắt
Từ khóa `super` trong Ruby được sử dụng để gọi phương thức cùng tên từ lớp cha trong ngữ cảnh của lớp con. Điều này giúp tối ưu hóa việc sử dụng kế thừa và tái sử dụng mã nguồn hiệu quả hơn.

## Tài Liệu
### Mục Đích
`super` cho phép lập trình viên gọi phương thức của lớp cha từ bên trong phương thức của lớp con, giúp duy trì tính kế thừa trong lập trình hướng đối tượng.

### Cách Sử Dụng
Cú pháp cơ bản của `super` là:
```ruby
super(arguments)
```
Nếu không có đối số nào được chỉ định, `super` sẽ tự động truyền tất cả các đối số mà phương thức hiện tại nhận được đến phương thức của lớp cha.

### Chi Tiết
- **Khi nào sử dụng**: Sử dụng `super` khi bạn muốn mở rộng hoặc sửa đổi hành vi của phương thức cha trong lớp con mà vẫn muốn giữ lại một phần của hành vi đó.
- **Phạm vi**: `super` chỉ có thể được sử dụng trong ngữ cảnh của các phương thức. Nếu bạn gọi `super` bên ngoài phương thức, Ruby sẽ phát sinh lỗi.
- **Hiệu suất**: Gọi `super` có thể ảnh hưởng đến hiệu suất nếu bạn có nhiều lớp cha, vì Ruby sẽ phải tìm kiếm trong cây kế thừa.

## Ví Dụ
### Ví dụ 1: Gọi phương thức cha
```ruby
class Animal
  def speak
    "Animal speaks"
  end
end

class Dog < Animal
  def speak
    super + " Woof!"
  end
end

dog = Dog.new
puts dog.speak  # Output: "Animal speaks Woof!"
```

### Ví dụ 2: Truyền đối số
```ruby
class Person
  def initialize(name)
    @name = name
  end
  
  def greet
    "Hello, #{@name}"
  end
end

class Student < Person
  def initialize(name, grade)
    super(name)
    @grade = grade
  end

  def greet
    super + " and I'm in grade #{@grade}"
  end
end

student = Student.new("Alice", 10)
puts student.greet  # Output: "Hello, Alice and I'm in grade 10"
```

## Giải Thích
Một số cạm bẫy thường gặp khi sử dụng `super`:
- **Quên gọi `super`**: Một số lập trình viên có thể quên gọi `super`, dẫn đến việc không thực hiện các hành vi cần thiết từ lớp cha.
- **Sử dụng sai ngữ cảnh**: Việc gọi `super` bên ngoài phương thức sẽ gây ra lỗi. Đảm bảo rằng bạn chỉ sử dụng `super` bên trong các phương thức.
- **Gọi `super` mà không có đối số**: Khi không có đối số, `super` sẽ tự động truyền các đối số từ phương thức hiện tại. Nếu bạn cần truyền các đối số khác, bạn cần chỉ định chúng rõ ràng.

## Tóm Tắt Ngắn Gọn
`super` trong Ruby là từ khóa cho phép gọi phương thức tương ứng từ lớp cha trong lớp con, giúp tối ưu hóa tính kế thừa trong lập trình hướng đối tượng.