<!--
Meta Description: # Hash trong Ruby: Cách sử dụng và ứng dụng ## Tóm tắt Hash trong Ruby là một cấu trúc dữ liệu cho phép lưu trữ cặp khóa-giá trị, giúp tổ chức và truy...
Meta Keywords: hash, một, ruby, khóa, giá
-->

# Hash trong Ruby: Cách sử dụng và ứng dụng

## Tóm tắt
Hash trong Ruby là một cấu trúc dữ liệu cho phép lưu trữ cặp khóa-giá trị, giúp tổ chức và truy cập dữ liệu một cách hiệu quả.

## Tài liệu
Hash là một kiểu dữ liệu quan trọng trong Ruby, cho phép bạn lưu trữ và quản lý dữ liệu theo cách mà bạn có thể dễ dàng truy cập bằng một khóa duy nhất. Mỗi khóa trong Hash là duy nhất và được liên kết với một giá trị. Hash rất linh hoạt và được sử dụng rộng rãi trong lập trình Ruby để lưu trữ thông tin một cách có cấu trúc.

### Cách tạo Hash
Bạn có thể tạo Hash bằng cách sử dụng dấu ngoặc nhọn `{}` hoặc phương thức `Hash.new`. Ví dụ:

```ruby
# Tạo hash bằng dấu ngoặc nhọn
my_hash = { "name" => "Alice", "age" => 30 }

# Tạo hash bằng phương thức Hash.new
my_hash = Hash.new
my_hash["name"] = "Alice"
my_hash["age"] = 30
```

### Truy cập giá trị
Để truy cập các giá trị trong Hash, bạn có thể sử dụng khóa tương ứng:

```ruby
puts my_hash["name"] # Kết quả: Alice
puts my_hash["age"]  # Kết quả: 30
```

### Các phương thức hữu ích
Ruby cung cấp nhiều phương thức để làm việc với Hash, bao gồm:
- `keys`: Trả về một mảng chứa tất cả các khóa.
- `values`: Trả về một mảng chứa tất cả các giá trị.
- `each`: Lặp qua từng cặp khóa-giá trị.

Ví dụ:

```ruby
my_hash.each do |key, value|
  puts "#{key}: #{value}"
end
```

## Ví dụ
Dưới đây là một số ví dụ về cách sử dụng Hash trong Ruby:

### Tạo và truy cập Hash
```ruby
person = { "name" => "Bob", "age" => 25 }
puts person["name"] # Kết quả: Bob
```

### Cập nhật giá trị
```ruby
person["age"] = 26
puts person["age"] # Kết quả: 26
```

### Thêm cặp khóa-giá trị mới
```ruby
person["city"] = "Hanoi"
puts person # Kết quả: {"name"=>"Bob", "age"=>26, "city"=>"Hanoi"}
```

## Giải thích
Mặc dù Hash là một công cụ mạnh mẽ, nhưng có một số điều cần lưu ý:
- Khóa trong Hash phải là duy nhất; nếu bạn khai báo một khóa trùng lặp, giá trị của khóa đó sẽ được cập nhật.
- Sử dụng không đúng kiểu dữ liệu cho khóa có thể dẫn đến lỗi không mong muốn. Ví dụ, sử dụng một đối tượng phức tạp như một khóa có thể gây khó khăn trong việc truy xuất giá trị.

## Tóm tắt một dòng
Hash trong Ruby là một cấu trúc dữ liệu linh hoạt giúp lưu trữ và quản lý cặp khóa-giá trị một cách hiệu quả.