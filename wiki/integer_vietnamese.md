<!--
Meta Description: # Integer trong Ruby: Tất cả những gì bạn cần biết ## Tóm tắt Trong Ruby, `Integer` là một lớp (class) đại diện cho các số nguyên. Nó cung cấp nhiều p...
Meta Keywords: nguyên, ruby, một, phép, integer
-->

# Integer trong Ruby: Tất cả những gì bạn cần biết

## Tóm tắt
Trong Ruby, `Integer` là một lớp (class) đại diện cho các số nguyên. Nó cung cấp nhiều phương thức hữu ích để thực hiện các phép toán và xử lý số nguyên một cách hiệu quả.

## Tài liệu
### Mục đích
Lớp `Integer` trong Ruby cho phép lập trình viên làm việc với các số nguyên, bao gồm việc thực hiện phép toán cơ bản, so sánh và chuyển đổi giữa các kiểu dữ liệu khác nhau. Ruby hỗ trợ số nguyên âm và dương, cũng như số nguyên lớn mà không bị giới hạn bởi kích thước bộ nhớ.

### Cách sử dụng
Để tạo một số nguyên trong Ruby, bạn chỉ cần gán một giá trị cho biến, ví dụ:
```ruby
num = 42
```
Bạn có thể thực hiện nhiều phép toán với số nguyên như cộng, trừ, nhân, chia, và nhiều hơn nữa:
```ruby
a = 10
b = 20

tong = a + b       # Cộng
hieu = a - b      # Trừ
tich = a * b      # Nhân
thuong = b / a    # Chia
```

### Chi tiết
Lớp `Integer` có nhiều phương thức tích hợp sẵn, ví dụ:
- `odd?`: Kiểm tra xem số có phải là số lẻ hay không.
- `even?`: Kiểm tra xem số có phải là số chẵn hay không.
- `to_s`: Chuyển đổi số nguyên thành chuỗi.
- `times`: Thực hiện một khối mã một số lần nhất định.

## Ví dụ
Dưới đây là một số ví dụ về cách sử dụng lớp `Integer` trong Ruby:

```ruby
# Khai báo số nguyên
number = 5

# Kiểm tra số chẵn
puts number.even?  # false

# Kiểm tra số lẻ
puts number.odd?   # true

# Chuyển đổi số thành chuỗi
puts number.to_s   # "5"

# Sử dụng phương thức `times`
number.times do |i|
  puts "Lần thứ #{i + 1}"
end
```

## Giải thích
Một số cạm bẫy thường gặp khi làm việc với `Integer` là:
- **Phép chia**: Khi chia hai số nguyên, Ruby sẽ trả về kết quả số nguyên, không làm tròn. Để có kết quả chính xác hơn, bạn có thể chuyển đổi một trong hai số sang loại số thực (float).
- **Kiểu dữ liệu**: Ruby tự động xác định kiểu dữ liệu, nhưng nếu bạn không cẩn thận, có thể sẽ gặp phải lỗi khi thực hiện các phép toán giữa các kiểu khác nhau (ví dụ: số nguyên và chuỗi).

## Tóm tắt một dòng
Lớp `Integer` trong Ruby cho phép lập trình viên thực hiện các phép toán và thao tác với số nguyên một cách linh hoạt và hiệu quả.