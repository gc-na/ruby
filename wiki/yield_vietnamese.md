<!--
Meta Description: # Hiểu về "yield" trong Ruby: Cách sử dụng và ứng dụng ## Tóm tắt "Yield" trong Ruby là một từ khóa mạnh mẽ cho phép bạn gọi một block (khối mã) từ bê...
Meta Keywords: yield, block, một, gọi, phương
-->

# Hiểu về "yield" trong Ruby: Cách sử dụng và ứng dụng

## Tóm tắt
"Yield" trong Ruby là một từ khóa mạnh mẽ cho phép bạn gọi một block (khối mã) từ bên trong một phương thức. Nó giúp thực hiện các tác vụ lặp lại một cách linh hoạt và hiệu quả.

## Tài liệu
### Mục đích
Từ khóa "yield" cho phép một phương thức truyền điều khiển cho một block mà nó nhận vào. Khi được gọi, phương thức sẽ tạm dừng và chuyển quyền điều khiển cho block, cho phép thực hiện mã trong block đó.

### Cách sử dụng
Để sử dụng "yield", bạn cần định nghĩa một phương thức và gọi "yield" bên trong đó. Block có thể được truyền vào phương thức khi được gọi.

### Chi tiết
- Khi một phương thức chứa từ khóa "yield" được gọi, Ruby sẽ tìm kiếm block tương ứng.
- Nếu không có block nào được cung cấp, việc gọi "yield" sẽ dẫn đến lỗi.
- Bạn có thể truyền tham số từ phương thức đến block bằng cách đặt chúng trong ngoặc đơn.

## Ví dụ
### Ví dụ cơ bản
```ruby
def greet
  yield("Hello")
end

greet { |message| puts message }  # Output: Hello
```

### Ví dụ với tham số
```ruby
def calculate_area(length, width)
  yield(length * width)
end

calculate_area(5, 10) { |area| puts "Diện tích là: #{area}" }  # Output: Diện tích là: 50
```

### Ví dụ với nhiều lần yield
```ruby
def repeat(n)
  n.times { yield }
end

repeat(3) { puts "Chào mừng!" }
# Output:
# Chào mừng!
# Chào mừng!
# Chào mừng!
```

## Giải thích
- **Lỗi khi không có block**: Nếu bạn quên cung cấp block khi gọi phương thức có sử dụng "yield", Ruby sẽ ném ra một lỗi `LocalJumpError`. Đảm bảo bạn luôn truyền block hoặc kiểm tra với `block_given?` trước khi gọi "yield".

### Lưu ý
- Bạn có thể sử dụng `return` trong block, nhưng lưu ý rằng nó sẽ trả về từ phương thức gọi block, không phải từ block.
- Việc sử dụng "yield" giúp giảm bớt độ phức tạp của mã và cải thiện khả năng đọc hiểu.

## Tóm tắt một câu
Từ khóa "yield" trong Ruby cho phép bạn gọi một block từ bên trong phương thức, giúp tạo ra mã linh hoạt và hiệu quả hơn.