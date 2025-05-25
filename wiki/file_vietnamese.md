<!--
Meta Description: # Hướng Dẫn Chi Tiết Về Lớp File Trong Ruby ## Tóm Tắt Lớp File trong Ruby cung cấp các phương thức để làm việc với các tệp tin trên hệ thống, cho phé...
Meta Keywords: tệp, file, ruby, ghi, với
-->

# Hướng Dẫn Chi Tiết Về Lớp File Trong Ruby

## Tóm Tắt
Lớp File trong Ruby cung cấp các phương thức để làm việc với các tệp tin trên hệ thống, cho phép đọc, ghi, và quản lý tệp tin một cách linh hoạt và dễ dàng.

## Tài Liệu
Lớp File là một phần quan trọng trong Ruby, cho phép lập trình viên tương tác với hệ thống tệp tin. Với File, bạn có thể thực hiện các thao tác như mở, đọc, ghi, và đóng tệp tin. Lớp này cũng hỗ trợ nhiều phương thức hữu ích để kiểm tra thông tin về tệp, chẳng hạn như kích thước, quyền truy cập, và thời gian sửa đổi.

### Cách Sử Dụng
Dưới đây là cú pháp cơ bản để sử dụng lớp File trong Ruby:

```ruby
File.open("tên_tệp", "chế độ") do |tệp|
  # Thao tác với tệp ở đây
end
```

Trong đó, "tên_tệp" là tên của tệp mà bạn muốn mở và "chế độ" xác định cách bạn muốn tương tác với tệp (ví dụ: đọc, ghi).

### Các Chế Độ Mở Tệp
- `"r"`: Chỉ đọc (read)
- `"w"`: Ghi (write) - tạo mới tệp hoặc ghi đè tệp cũ
- `"a"`: Ghi bổ sung (append) - ghi vào cuối tệp
- `"r+"`: Đọc và ghi (read and write)

## Ví Dụ
Dưới đây là một số ví dụ đơn giản về cách sử dụng lớp File trong Ruby:

### Đọc Tệp
```ruby
File.open("example.txt", "r") do |file|
  content = file.read
  puts content
end
```

### Ghi Tệp
```ruby
File.open("example.txt", "w") do |file|
  file.write("Chào mừng đến với Ruby!")
end
```

### Ghi Bổ Sung
```ruby
File.open("example.txt", "a") do |file|
  file.puts("Dòng mới được thêm vào.")
end
```

## Giải Thích
Khi làm việc với lớp File, có một số điều cần lưu ý:
- Đảm bảo tệp tồn tại trước khi đọc để tránh lỗi. Sử dụng phương thức `File.exist?` để kiểm tra.
- Khi mở tệp với chế độ `"w"`, nội dung cũ sẽ bị xóa. Nếu bạn muốn giữ lại nội dung cũ, hãy sử dụng chế độ `"a"`.
- Luôn đóng tệp sau khi hoàn thành thao tác để giải phóng tài nguyên.

## Tóm Tắt Một Dòng
Lớp File trong Ruby cho phép bạn dễ dàng thực hiện các thao tác với tệp tin, bao gồm đọc, ghi, và quản lý tệp một cách hiệu quả.