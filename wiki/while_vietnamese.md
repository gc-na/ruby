<!--
Meta Description: # Câu lệnh "while" trong Ruby: Cách sử dụng và ví dụ ## Tóm tắt Câu lệnh "while" trong Ruby cho phép thực hiện một khối mã nhiều lần dựa trên điều kiệ...
Meta Keywords: điều, kiện, while, khi, câu
-->

# Câu lệnh "while" trong Ruby: Cách sử dụng và ví dụ

## Tóm tắt
Câu lệnh "while" trong Ruby cho phép thực hiện một khối mã nhiều lần dựa trên điều kiện xác định, giúp lập trình viên kiểm soát luồng thực thi của chương trình.

## Tài liệu
Câu lệnh "while" trong Ruby được sử dụng để lặp lại một đoạn mã cho đến khi điều kiện trong biểu thức trở thành sai. Cấu trúc của câu lệnh "while" rất đơn giản:

```ruby
while điều_kiện
  # mã thực thi
end
```

### Mục đích
Mục đích chính của câu lệnh "while" là để thực hiện lặp lại một khối mã cho đến khi điều kiện không còn đúng. Điều này rất hữu ích trong nhiều tình huống, chẳng hạn như khi bạn cần xử lý dữ liệu cho đến khi một điều kiện nhất định được thỏa mãn.

### Cách sử dụng
- **Điều kiện**: Biểu thức điều kiện được kiểm tra trước khi thực hiện khối mã. Nếu điều kiện đúng (true), khối mã sẽ được thực hiện.
- **Kết thúc vòng lặp**: Vòng lặp sẽ tiếp tục cho đến khi điều kiện trở thành sai (false). Để tránh vòng lặp vô hạn, bạn cần đảm bảo rằng điều kiện sẽ trở thành sai tại một thời điểm nào đó.

## Ví dụ
### Ví dụ cơ bản 1: Đếm từ 1 đến 5

```ruby
i = 1
while i <= 5 do
  puts i
  i += 1
end
```

### Ví dụ cơ bản 2: Nhập liệu cho đến khi người dùng nhập "exit"

```ruby
input = ""
while input != "exit" do
  puts "Nhập một cái gì đó (hoặc 'exit' để thoát):"
  input = gets.chomp
end
```

## Giải thích
### Những cạm bẫy phổ biến
- **Vòng lặp vô hạn**: Nếu điều kiện trong câu lệnh "while" luôn đúng mà không có cách nào để thoát khỏi, mã sẽ gây ra vòng lặp vô hạn, làm treo chương trình.
- **Không khởi tạo biến**: Nếu biến điều kiện không được khởi tạo trước khi vào vòng lặp, bạn có thể gặp phải lỗi không xác định.
  
### Các ghi chú bổ sung
- Sử dụng câu lệnh "break" bên trong vòng lặp để thoát ra khi cần thiết.
- Câu lệnh "while" có thể được kết hợp với câu lệnh "else" để thực hiện một đoạn mã khi điều kiện sai.

## Tóm tắt một dòng
Câu lệnh "while" trong Ruby cho phép thực hiện lặp lại một khối mã cho đến khi điều kiện trở thành sai, rất hữu ích trong việc kiểm soát luồng thực thi của chương trình.