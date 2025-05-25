<!--
Meta Description: # Chuỗi (String) trong Ruby: Hướng Dẫn Chi Tiết và Cách Sử Dụng ## Tóm Tắt Chuỗi (String) trong Ruby là một kiểu dữ liệu quan trọng cho phép lưu trữ v...
Meta Keywords: chuỗi, ruby, một, đổi, nháy
-->

# Chuỗi (String) trong Ruby: Hướng Dẫn Chi Tiết và Cách Sử Dụng

## Tóm Tắt
Chuỗi (String) trong Ruby là một kiểu dữ liệu quan trọng cho phép lưu trữ và thao tác với các dãy ký tự. Ruby cung cấp nhiều phương thức mạnh mẽ để làm việc với chuỗi, giúp lập trình viên dễ dàng xử lý và thao tác trên văn bản.

## Tài Liệu
Chuỗi trong Ruby là một kiểu dữ liệu cơ bản dùng để biểu diễn văn bản. Mỗi chuỗi có thể được tạo ra bằng cách sử dụng dấu nháy đơn (`'`) hoặc dấu nháy kép (`"`). Việc sử dụng dấu nháy kép cho phép bạn nhúng các biến và thực hiện các phép biến đổi đặc biệt như `\n` cho xuống dòng.

### Tạo Chuỗi
Bạn có thể tạo chuỗi bằng cách:
```ruby
str1 = 'Xin chào'
str2 = "Thời gian hiện tại: #{Time.now}"
```

### Một số phương thức phổ biến:
- `length`: Trả về độ dài của chuỗi.
- `upcase`: Chuyển đổi tất cả ký tự thành chữ hoa.
- `downcase`: Chuyển đổi tất cả ký tự thành chữ thường.
- `strip`: Xóa khoảng trắng ở đầu và cuối chuỗi.
- `gsub`: Thay thế một chuỗi con bằng một chuỗi khác.

### Ví dụ Sử Dụng:
```ruby
# Tạo chuỗi
greeting = "Xin chào, Ruby!"

# Lấy độ dài của chuỗi
puts greeting.length  # Kết quả: 18

# Chuyển đổi thành chữ hoa
puts greeting.upcase   # Kết quả: XIN CHÀO, RUBY!

# Thay thế chuỗi
new_greeting = greeting.gsub("Ruby", "Thế giới")
puts new_greeting      # Kết quả: Xin chào, Thế giới!
```

## Giải Thích
Mặc dù Ruby cung cấp nhiều phương thức để làm việc với chuỗi, nhưng có một số điều cần lưu ý:

- **Sự khác biệt giữa dấu nháy đơn và nháy kép**: Dấu nháy đơn sẽ không thực hiện phép biến đổi, trong khi dấu nháy kép sẽ.
- **Biến đổi không thay đổi chuỗi gốc**: Hầu hết các phương thức như `upcase`, `downcase`, và `strip` sẽ không thay đổi chuỗi gốc mà sẽ trả về một chuỗi mới.
- **Chú ý đến mã hóa**: Ruby hỗ trợ nhiều mã hóa ký tự, hãy chắc chắn rằng bạn đang làm việc với mã hóa phù hợp, đặc biệt khi xử lý văn bản đa ngôn ngữ.

## Tóm Tắt Một Dòng
Chuỗi (String) trong Ruby là kiểu dữ liệu quan trọng cho phép lưu trữ và thao tác với dãy ký tự, đi kèm với nhiều phương thức mạnh mẽ để xử lý văn bản.