<!--
Meta Description: # Lệnh "rescue" trong Ruby: Cách xử lý ngoại lệ hiệu quả ## Tóm tắt Lệnh "rescue" trong Ruby được sử dụng để xử lý các ngoại lệ (exceptions) trong chư...
Meta Keywords: rescue, ngoại, lỗi, ruby, puts
-->

# Lệnh "rescue" trong Ruby: Cách xử lý ngoại lệ hiệu quả

## Tóm tắt
Lệnh "rescue" trong Ruby được sử dụng để xử lý các ngoại lệ (exceptions) trong chương trình, giúp lập trình viên kiểm soát các tình huống lỗi mà không làm dừng hoạt động của ứng dụng.

## Tài liệu
Lệnh "rescue" là một phần quan trọng trong hệ thống xử lý lỗi của Ruby. Nó cho phép người dùng bắt các ngoại lệ và thực hiện các hành động nhất định khi những ngoại lệ này xảy ra. Cú pháp cơ bản của lệnh "rescue" là:

```ruby
begin
  # Mã có thể gây ra ngoại lệ
rescue SomeExceptionClass => e
  # Xử lý ngoại lệ
end
```

### Mục đích
Mục đích chính của "rescue" là để bảo vệ chương trình khỏi việc bị dừng đột ngột khi gặp lỗi, đồng thời cho phép lập trình viên thực hiện các hành động khắc phục hoặc ghi lại thông tin lỗi.

### Cách sử dụng
- **Bắt ngoại lệ cụ thể**: Bạn có thể chỉ định loại ngoại lệ mà bạn muốn bắt, ví dụ:
  ```ruby
  begin
    # Mã có thể gây ra ngoại lệ
  rescue ZeroDivisionError => e
    puts "Lỗi chia cho 0: #{e.message}"
  end
  ```

- **Bắt tất cả ngoại lệ**: Nếu bạn không chỉ định loại ngoại lệ, Ruby sẽ bắt tất cả các ngoại lệ:
  ```ruby
  begin
    # Mã có thể gây ra ngoại lệ
  rescue => e
    puts "Đã xảy ra lỗi: #{e.message}"
  end
  ```

- **Nhiều rescue**: Bạn cũng có thể có nhiều khối rescue để xử lý các loại ngoại lệ khác nhau:
  ```ruby
  begin
    # Mã có thể gây ra ngoại lệ
  rescue ZeroDivisionError => e
    puts "Lỗi chia cho 0: #{e.message}"
  rescue StandardError => e
    puts "Lỗi khác: #{e.message}"
  end
  ```

## Ví dụ
### Ví dụ 1: Bắt ngoại lệ chia cho 0
```ruby
begin
  puts 10 / 0
rescue ZeroDivisionError => e
  puts "Lỗi: #{e.message}"
end
```

### Ví dụ 2: Bắt tất cả các loại ngoại lệ
```ruby
begin
  puts "Kết quả: #{10 / 0}"
rescue => e
  puts "Đã xảy ra lỗi: #{e.message}"
end
```

### Ví dụ 3: Nhiều khối rescue
```ruby
begin
  puts "Nhập số: "
  num = gets.to_i
  puts 10 / num
rescue ZeroDivisionError => e
  puts "Lỗi chia cho 0: #{e.message}"
rescue StandardError => e
  puts "Lỗi không xác định: #{e.message}"
end
```

## Giải thích
Một số điểm cần lưu ý khi sử dụng lệnh "rescue":
- **Thứ tự khối rescue**: Khi sử dụng nhiều khối rescue, thứ tự rất quan trọng. Ruby sẽ kiểm tra từ trên xuống và thực hiện khối đầu tiên phù hợp với ngoại lệ xảy ra.
- **Không bắt ngoại lệ**: Nếu bạn không bắt ngoại lệ, chương trình sẽ bị dừng và thông báo lỗi sẽ được in ra console.
- **Rescue trong khối method**: Bạn có thể sử dụng rescue trong các phương thức để dễ dàng quản lý lỗi trong các phần của ứng dụng lớn hơn.

## Tóm tắt một dòng
Lệnh "rescue" trong Ruby giúp lập trình viên xử lý ngoại lệ một cách hiệu quả, ngăn chặn việc dừng chương trình khi gặp lỗi.