<!--
Meta Description: # Câu lệnh "if" trong Ruby: Cách Sử Dụng và Ví Dụ Thực Tế ## Tóm tắt Câu lệnh "if" trong Ruby là một cấu trúc điều kiện cho phép thực thi một đoạn mã ...
Meta Keywords: điều, kiện, ruby, một, trong
-->

# Câu lệnh "if" trong Ruby: Cách Sử Dụng và Ví Dụ Thực Tế

## Tóm tắt
Câu lệnh "if" trong Ruby là một cấu trúc điều kiện cho phép thực thi một đoạn mã khi điều kiện cho trước là đúng. Đây là một trong những công cụ cơ bản và quan trọng nhất trong lập trình để kiểm soát luồng chương trình.

## Tài liệu
Câu lệnh "if" trong Ruby được sử dụng để kiểm tra một điều kiện và thực hiện một đoạn mã khi điều kiện đó đúng (true). Cú pháp cơ bản của câu lệnh "if" như sau:

```ruby
if điều_kiện
  # đoạn mã thực hiện khi điều kiện đúng
end
```

### Cú pháp mở rộng
Ruby cũng hỗ trợ các cấu trúc điều kiện mở rộng như `elsif` và `else`, cho phép kiểm tra nhiều điều kiện:

```ruby
if điều_kiện_1
  # đoạn mã thực hiện khi điều kiện 1 đúng
elsif điều_kiện_2
  # đoạn mã thực hiện khi điều kiện 2 đúng
else
  # đoạn mã thực hiện khi không có điều kiện nào đúng
end
```

### Kiểm tra điều kiện
Điều kiện có thể là bất kỳ biểu thức nào trả về giá trị boolean (true hoặc false). Bạn cũng có thể kết hợp nhiều điều kiện với toán tử logic như `&&` (và), `||` (hoặc).

## Ví dụ
Dưới đây là một số ví dụ đơn giản về cách sử dụng câu lệnh "if":

### Ví dụ 1: Kiểm tra số
```ruby
num = 10
if num > 5
  puts "Số lớn hơn 5"
end
```

### Ví dụ 2: Sử dụng elsif và else
```ruby
num = 3
if num > 5
  puts "Số lớn hơn 5"
elsif num == 5
  puts "Số bằng 5"
else
  puts "Số nhỏ hơn 5"
end
```

### Ví dụ 3: Kết hợp nhiều điều kiện
```ruby
age = 20
if age >= 18 && age < 65
  puts "Đối tượng đủ tuổi lao động"
else
  puts "Đối tượng không đủ tuổi lao động"
end
```

## Giải thích
Một số lưu ý khi sử dụng câu lệnh "if" trong Ruby:

- **Indentation**: Mặc dù không bắt buộc, việc căn chỉnh đoạn mã sẽ giúp dễ đọc và dễ quản lý hơn.
- **Biểu thức boolean**: Hãy chắc chắn rằng điều kiện bạn kiểm tra trả về giá trị boolean. Ví dụ, `if 5` sẽ luôn đúng vì bất kỳ giá trị nào khác `nil` và `false` đều được coi là đúng.
- **Giá trị trả về**: Câu lệnh "if" cũng có thể trả về giá trị. Điều này có nghĩa là bạn có thể sử dụng nó như một biểu thức trong Ruby.

## Tóm tắt một dòng
Câu lệnh "if" trong Ruby cho phép thực hiện đoạn mã dựa trên việc kiểm tra một điều kiện boolean, rất hữu ích trong việc kiểm soát luồng chương trình.