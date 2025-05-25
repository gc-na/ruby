<!--
Meta Description: # Câu lệnh "ensure" trong Ruby: Cách sử dụng và ứng dụng ## Tóm tắt Câu lệnh `ensure` trong Ruby được sử dụng để đảm bảo rằng một khối mã nhất định sẽ...
Meta Keywords: ensure, được, trong, khối, dụng
-->

# Câu lệnh "ensure" trong Ruby: Cách sử dụng và ứng dụng

## Tóm tắt
Câu lệnh `ensure` trong Ruby được sử dụng để đảm bảo rằng một khối mã nhất định sẽ được thực thi, bất kể kết quả của các khối mã khác (như `begin` hoặc `rescue`). Điều này rất hữu ích trong việc quản lý tài nguyên và xử lý ngoại lệ.

## Tài liệu
### Mục đích
Câu lệnh `ensure` cho phép lập trình viên đảm bảo rằng một đoạn mã sẽ luôn được thực thi, ngay cả khi có một ngoại lệ xảy ra trong khối mã trước đó. Điều này giúp bảo vệ tài nguyên như tệp tin, kết nối cơ sở dữ liệu, hoặc bất kỳ tài nguyên nào cần phải được giải phóng hoặc đóng lại.

### Cách sử dụng
Cú pháp cơ bản của `ensure` như sau:

```ruby
begin
  # Khối mã có thể gây ra ngoại lệ
rescue => e
  # Xử lý ngoại lệ
ensure
  # Khối mã sẽ luôn được thực thi
end
```

## Ví dụ
### Ví dụ cơ bản
Dưới đây là một ví dụ đơn giản về cách sử dụng `ensure`:

```ruby
begin
  file = File.open("test.txt", "r")
  # Đọc nội dung tệp
  content = file.read
  puts content
rescue => e
  puts "Đã xảy ra lỗi: #{e.message}"
ensure
  file.close if file
  puts "Tệp đã được đóng."
end
```

Trong ví dụ trên, tệp `test.txt` sẽ được đóng dù có xảy ra lỗi hay không trong quá trình đọc nội dung.

## Giải thích
### Những cạm bẫy phổ biến
- **Quên kiểm tra tài nguyên**: Nếu bạn không kiểm tra xem tài nguyên có được khởi tạo hay không trước khi gọi `close`, bạn có thể gặp lỗi `NoMethodError`. Đó là lý do tại sao chúng ta thường sử dụng điều kiện `if file` trước khi gọi `file.close`.
- **Sự nhầm lẫn với `else`**: Đừng nhầm lẫn giữa `ensure` và `else` trong Ruby. Khối `else` chỉ thực thi nếu không có ngoại lệ xảy ra, trong khi `ensure` sẽ luôn thực thi.

### Ghi chú thêm
- `ensure` có thể được sử dụng không chỉ trong khối `begin-rescue`, mà còn trong các phương thức để đảm bảo rằng một số hành động sẽ luôn diễn ra.
- `ensure` có thể được sử dụng với nhiều khối mã khác nhau, nhưng chỉ có một khối `ensure` có thể được chỉ định cho mỗi khối `begin`.

## Tóm tắt ngắn gọn
Câu lệnh `ensure` trong Ruby đảm bảo rằng một đoạn mã sẽ luôn được thực thi, cung cấp một cách hiệu quả để quản lý tài nguyên và xử lý ngoại lệ.