<!--
Meta Description: # Float trong Ruby: Tìm Hiểu Kiểu Dữ Liệu Số Thực ## Tóm Tắt Float trong Ruby là kiểu dữ liệu đại diện cho các số thực, cho phép lưu trữ và thực hiện ...
Meta Keywords: ruby, float, các, phép, toán
-->

# Float trong Ruby: Tìm Hiểu Kiểu Dữ Liệu Số Thực

## Tóm Tắt
Float trong Ruby là kiểu dữ liệu đại diện cho các số thực, cho phép lưu trữ và thực hiện các phép toán với số có phần thập phân.

## Tài Liệu
Float là một kiểu dữ liệu trong Ruby được sử dụng để lưu trữ các số thực (số có phần thập phân). Kiểu này rất hữu ích trong các ứng dụng cần tính toán chính xác với số liệu liên quan đến khoa học, tài chính, hoặc bất kỳ lĩnh vực nào yêu cầu độ chính xác cao trong phép toán. 

### Cách Sử Dụng
Để khai báo một biến kiểu Float, bạn có thể gán giá trị số thực cho biến đó. Ruby tự động nhận diện kiểu dữ liệu này khi bạn sử dụng số có phần thập phân.

```ruby
a = 3.14
b = 2.0
```

### Chi Tiết
- **Khởi Tạo**: Float có thể được khởi tạo bằng cách sử dụng số có dấu thập phân (`3.14`, `0.5`), hoặc bằng hàm `Float()`:
    ```ruby
    c = Float("2.71828")
    ```

- **Phép Toán**: Float hỗ trợ các phép toán cơ bản như cộng, trừ, nhân, chia:
    ```ruby
    sum = a + b    # 5.14
    product = a * b  # 6.28
    ```

- **So Sánh**: Bạn có thể sử dụng các toán tử so sánh để so sánh các giá trị Float:
    ```ruby
    if a > b
      puts "#{a} lớn hơn #{b}"
    end
    ```

## Ví Dụ
### Khởi Tạo và Sử Dụng
```ruby
x = 10.5
y = 2.5
result = x / y  # Kết quả: 4.2
puts result
```

### Phép Toán
```ruby
a = 5.0
b = 2.0
puts a + b  # Kết quả: 7.0
puts a - b  # Kết quả: 3.0
puts a * b  # Kết quả: 10.0
puts a / b  # Kết quả: 2.5
```

### So Sánh
```ruby
a = 1.5
b = 2.5
if a < b
  puts "#{a} nhỏ hơn #{b}"
end
```

## Giải Thích
Một số vấn đề thường gặp khi làm việc với Float trong Ruby:
- **Độ Chính Xác**: Float có thể gặp vấn đề về độ chính xác trong các phép toán, đặc biệt là khi thực hiện phép cộng hoặc trừ với các số lớn hoặc rất nhỏ. Điều này là do cách mà máy tính lưu trữ số thực.
- **Phép Làm Tròn**: Khi chuyển đổi giữa kiểu dữ liệu, có thể xảy ra hiện tượng làm tròn không mong muốn. Sử dụng các phương thức như `round`, `ceil`, và `floor` có thể giúp kiểm soát điều này.
  
```ruby
# Ví dụ về làm tròn
x = 2.675
puts x.round(2)  # Kết quả: 2.67 (không phải 2.68 như mong đợi)
```

## Tóm Tắt Một Dòng
Float trong Ruby là kiểu dữ liệu cho phép lưu trữ và thực hiện các phép toán với số thực, rất cần thiết cho các ứng dụng yêu cầu tính toán chính xác.