<!--
Meta Description: # Numeric trong Ruby: Tất cả những gì bạn cần biết ## Tóm tắt Numeric là một lớp cơ bản trong Ruby đại diện cho các kiểu số học như Integer, Float, và...
Meta Keywords: các, kiểu, phương, thức, phép
-->

# Numeric trong Ruby: Tất cả những gì bạn cần biết

## Tóm tắt
Numeric là một lớp cơ bản trong Ruby đại diện cho các kiểu số học như Integer, Float, và Rational. Lớp này cung cấp các phương thức cho phép thực hiện các phép toán số học và so sánh.

## Tài liệu
### Mục đích
Lớp Numeric trong Ruby là lớp cha cho các kiểu số học khác nhau, cung cấp một bộ phương thức hữu ích cho việc xử lý và tính toán số.

### Sử dụng
Để sử dụng lớp Numeric, bạn có thể tạo một đối tượng thuộc các kiểu số như Integer hoặc Float. Lớp này hỗ trợ nhiều phép toán và phương thức để làm việc với các giá trị số.

### Chi tiết
- **Phương thức cơ bản**: Numeric cung cấp các phương thức như `+, -, *, /, %` để thực hiện các phép toán cơ bản.
- **So sánh**: Bạn có thể sử dụng các phương thức như `<`, `>`, `<=`, `>=`, `==`, và `!=` để so sánh các số.
- **Chuyển đổi kiểu**: Numeric hỗ trợ chuyển đổi giữa các kiểu số khác nhau, chẳng hạn như từ Integer sang Float với phương thức `to_f`.

## Ví dụ
```ruby
# Tạo các số nguyên và số thực
a = 10         # Integer
b = 3.14      # Float

# Thực hiện các phép toán
sum = a + b               # => 13.14
difference = a - b        # => 6.86
product = a * b           # => 31.4
quotient = a / b         # => 3.183098861837907
modulus = a % 3           # => 1

# So sánh
is_equal = (a == 10)     # => true
is_greater = (b > 2)     # => true
```

## Giải thích
- **Lưu ý về kiểu số**: Khi thực hiện phép chia giữa hai số nguyên, kết quả sẽ là một số nguyên trong Ruby. Để có kết quả chính xác, bạn cần ít nhất một trong hai số phải là kiểu Float.
- **Tránh việc chia cho 0**: Khi thực hiện phép chia, hãy đảm bảo rằng mẫu số không phải là 0, vì điều này sẽ gây ra lỗi.

## Tóm tắt một dòng
Numeric trong Ruby là lớp cha cho các kiểu số, cung cấp các phương thức để thực hiện các phép toán và so sánh số học.