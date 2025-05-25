<!--
Meta Description: # Tải (load) trong Ruby: Cách sử dụng và ứng dụng ## Tóm tắt Lệnh `load` trong Ruby cho phép người dùng tải và thực thi một tệp mã nguồn Ruby. Lệnh nà...
Meta Keywords: tệp, load, nạp, ruby, trong
-->

# Tải (load) trong Ruby: Cách sử dụng và ứng dụng

## Tóm tắt
Lệnh `load` trong Ruby cho phép người dùng tải và thực thi một tệp mã nguồn Ruby. Lệnh này hữu ích cho việc phát triển và thử nghiệm mã, cho phép bạn nạp lại mã mà không cần khởi động lại chương trình.

## Tài liệu
### Mục đích
Lệnh `load` được sử dụng để nạp một tệp Ruby và thực thi nó trong ngữ cảnh hiện tại. Điều này có nghĩa là các định nghĩa biến, phương thức và lớp trong tệp được nạp sẽ có sẵn ngay lập tức.

### Cú pháp
```ruby
load(filepath, wrap = false)
```

- `filepath`: Đường dẫn đến tệp Ruby cần nạp. Có thể là đường dẫn tuyệt đối hoặc tương đối.
- `wrap`: (Tùy chọn) Nếu được đặt là `true`, mã sẽ được chạy trong một khối riêng biệt, điều này giúp bảo vệ khỏi xung đột biến.

### Chi tiết
- Khi sử dụng `load`, Ruby sẽ kiểm tra xem tệp đã được nạp hay chưa. Nếu đã nạp, tệp sẽ được nạp lại mỗi lần `load` được gọi, khác với lệnh `require`, nơi mà tệp chỉ được nạp một lần.
- Điều này làm cho `load` trở thành công cụ hữu ích trong quá trình phát triển để thử nghiệm mã mà không cần khởi động lại chương trình.
- Tuy nhiên, vì `load` có thể nạp lại tệp nhiều lần, điều này có thể dẫn đến các vấn đề về hiệu suất và xung đột tên.

## Ví dụ
### Ví dụ cơ bản
```ruby
# Tạo một tệp có tên example.rb
# example.rb
def hello
  puts "Xin chào, thế giới!"
end

# Sử dụng lệnh load trong tệp chính
load 'example.rb'
hello  # Kết quả: Xin chào, thế giới!
```

### Nạp lại tệp
```ruby
# Tệp example.rb
def hello
  puts "Xin chào"
end

# Tệp chính
load 'example.rb'
hello  # Kết quả: Xin chào

# Thay đổi nội dung của example.rb thành "Xin chào, Ruby!"
load 'example.rb'
hello  # Kết quả: Xin chào, Ruby!
```

## Giải thích
- **Xung đột tên**: Nếu bạn có biến hoặc phương thức trùng tên trong tệp đã nạp, việc nạp lại tệp có thể dẫn đến xung đột không mong muốn, gây ra lỗi hoặc hành vi không chính xác.
- **Hiệu suất**: Sử dụng `load` nhiều lần có thể làm giảm hiệu suất của ứng dụng, đặc biệt là với các tệp lớn hoặc phức tạp.
- **Khác biệt với require**: Khác với `require`, `load` sẽ không kiểm tra nếu tệp đã được nạp hay chưa, điều này có thể dẫn đến việc thực thi mã không cần thiết và có thể gây ra lỗi.

## Tóm tắt một dòng
Lệnh `load` trong Ruby cho phép nạp và thực thi tệp mã nguồn, hữu ích cho việc phát triển và thử nghiệm mã.