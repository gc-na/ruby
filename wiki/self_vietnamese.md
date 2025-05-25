<!--
Meta Description: # Từ Khóa "self" Trong Ruby: Hiểu Về Cách Thức Hoạt Động Của Nó ## Tóm Tắt Trong ngôn ngữ lập trình Ruby, từ khóa `self` được sử dụng để tham chiếu đế...
Meta Keywords: self, thức, trong, phương, dụng
-->

# Từ Khóa "self" Trong Ruby: Hiểu Về Cách Thức Hoạt Động Của Nó

## Tóm Tắt
Trong ngôn ngữ lập trình Ruby, từ khóa `self` được sử dụng để tham chiếu đến đối tượng hiện tại của lớp hoặc module. Điều này cho phép người lập trình truy cập vào các phương thức và thuộc tính của đối tượng mà không cần phải chỉ định tên đối tượng.

## Tài Liệu
### Mục Đích
Từ khóa `self` cho phép bạn làm việc với đối tượng hiện tại mà không cần phải đặt tên cho nó. Điều này cực kỳ hữu ích trong các phương thức, cho phép bạn truy cập các thuộc tính và phương thức khác của đối tượng.

### Cách Sử Dụng
`self` có thể được sử dụng ở nhiều ngữ cảnh khác nhau:

- Trong một phương thức instance, `self` đại diện cho đối tượng của lớp đang gọi phương thức đó.
- Trong một phương thức class, `self` đại diện cho lớp đó.
- Khi được sử dụng trong một block, `self` có thể đại diện cho đối tượng mà block được gọi.

### Chi Tiết
- `self` không chỉ là một biến; nó là một từ khóa có nghĩa đặc biệt trong Ruby.
- Bạn có thể sử dụng `self` để xác định các phương thức lớp bằng cách định nghĩa các phương thức với `self.method_name`.
- Trong các block, `self` có thể thay đổi tùy theo ngữ cảnh gọi block.

## Ví Dụ
### Ví dụ 1: Sử Dụng `self` Trong Phương Thức Instance
```ruby
class Dog
  def initialize(name)
    @name = name
  end

  def bark
    puts "#{self.name} says woof!"
  end

  def name
    @name
  end
end

dog = Dog.new("Buddy")
dog.bark  # Kết quả: Buddy says woof!
```

### Ví dụ 2: Sử Dụng `self` Trong Phương Thức Class
```ruby
class Dog
  def self.species
    "Canis lupus familiaris"
  end
end

puts Dog.species  # Kết quả: Canis lupus familiaris
```

### Ví dụ 3: Sử Dụng `self` Trong Block
```ruby
class Counter
  attr_accessor :count

  def initialize
    @count = 0
  end

  def increment
    self.count += 1
  end
end

counter = Counter.new
counter.increment
puts counter.count  # Kết quả: 1
```

## Giải Thích
- **Cạm Bẫy Thường Gặp**: Một số người mới bắt đầu có thể nhầm lẫn giữa `self` và `self.class`. Hãy nhớ rằng `self` tham chiếu đến đối tượng hiện tại, trong khi `self.class` trả về lớp của đối tượng đó.
- **Thay Đổi Ngữ Cảnh**: Khi sử dụng `self` trong block, hãy chú ý rằng nó có thể tham chiếu đến một đối tượng khác nếu không được sử dụng cẩn thận.
- **Phương Thức Class**: Khi sử dụng `self` để định nghĩa phương thức class, bạn không cần phải tạo một instance của lớp để gọi phương thức đó.

## Tóm Tắt Một Câu
Từ khóa `self` trong Ruby cho phép bạn tham chiếu đến đối tượng hiện tại, giúp truy cập các phương thức và thuộc tính một cách dễ dàng và hiệu quả.