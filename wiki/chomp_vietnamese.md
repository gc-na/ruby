<!--
Meta Description: # Chức Năng Chomp trong Ruby: Xóa Ký Tự Kết Thúc Chuỗi ## Tóm Tắt Chức năng `chomp` trong Ruby được sử dụng để loại bỏ ký tự kết thúc chuỗi, thường là...
Meta Keywords: chomp, chuỗi, kết, không, thúc
-->

# Chức Năng Chomp trong Ruby: Xóa Ký Tự Kết Thúc Chuỗi

## Tóm Tắt
Chức năng `chomp` trong Ruby được sử dụng để loại bỏ ký tự kết thúc chuỗi, thường là ký tự newline (`\n`) hoặc ký tự carriage return (`\r`). Đây là một công cụ hữu ích khi làm việc với đầu vào từ người dùng hoặc dữ liệu từ tệp.

## Tài Liệu
### Mục Đích
`chomp` giúp làm sạch chuỗi bằng cách loại bỏ các ký tự không cần thiết ở cuối chuỗi. Điều này rất quan trọng trong việc xử lý dữ liệu, đặc biệt khi bạn muốn tránh các lỗi do ký tự kết thúc không mong muốn.

### Cách Sử Dụng
Cú pháp cơ bản của `chomp` như sau:

```ruby
string.chomp([separator])
```

- `string`: Chuỗi cần xử lý.
- `[separator]`: (Tùy chọn) Ký tự hoặc chuỗi cần xóa. Nếu không có tham số nào được cung cấp, `chomp` sẽ mặc định xóa ký tự newline.

### Chi Tiết
- `chomp` trả về một bản sao của chuỗi mà không có ký tự kết thúc được chỉ định.
- Nếu chuỗi không kết thúc bằng ký tự được chỉ định, chuỗi gốc sẽ được trả về mà không bị thay đổi.
- `chomp!` là phiên bản bang tính của `chomp`, sẽ thay đổi chuỗi gốc nếu có ký tự kết thúc được loại bỏ.

## Ví Dụ
### Ví dụ Cơ Bản
```ruby
# Ví dụ 1: Sử dụng chomp để loại bỏ ký tự newline
input = "Hello, World!\n"
cleaned_input = input.chomp
puts cleaned_input  # Kết quả: "Hello, World!"

# Ví dụ 2: Sử dụng chomp với ký tự chỉ định
input = "Hello, World!\r"
cleaned_input = input.chomp("\r")
puts cleaned_input  # Kết quả: "Hello, World!"
```

### Ví dụ với chomp!
```ruby
# Ví dụ 3: Sử dụng chomp! để thay đổi chuỗi gốc
input = "Hello, World!\n"
input.chomp!
puts input  # Kết quả: "Hello, World!"
```

## Giải Thích
Một số lưu ý và lỗi thường gặp khi sử dụng `chomp`:
- Nếu bạn quên cung cấp ký tự kết thúc mà bạn muốn loại bỏ, `chomp` sẽ chỉ loại bỏ ký tự newline, có thể không phải là điều bạn mong muốn.
- Khi sử dụng `chomp!`, nếu không có ký tự nào được loại bỏ, phương thức sẽ trả về `nil`. Do đó, bạn có thể cần kiểm tra giá trị trả về nếu muốn biết liệu chuỗi đã được thay đổi hay chưa.
- `chomp` không thay đổi chuỗi gốc mà chỉ trả về một bản sao, trong khi `chomp!` thay đổi chuỗi gốc.

## Tóm Tắt Một Dòng
Chức năng `chomp` trong Ruby giúp loại bỏ ký tự kết thúc không mong muốn từ chuỗi, làm sạch dữ liệu đầu vào cho các thao tác tiếp theo.