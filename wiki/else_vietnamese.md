<!--
Meta Description: # Câu Lệnh "else" Trong Ruby: Cách Sử Dụng và Ví Dụ ## Tóm Tắt Câu lệnh "else" trong Ruby được sử dụng để định nghĩa một khối mã sẽ được thực thi khi ...
Meta Keywords: điều, câu, lệnh, kiện, else
-->

# Câu Lệnh "else" Trong Ruby: Cách Sử Dụng và Ví Dụ

## Tóm Tắt
Câu lệnh "else" trong Ruby được sử dụng để định nghĩa một khối mã sẽ được thực thi khi điều kiện trong câu lệnh "if" không được thỏa mãn. Đây là một phần quan trọng trong việc kiểm soát luồng chương trình.

## Tài Liệu
Câu lệnh "else" là một phần của cấu trúc điều kiện trong Ruby, cho phép lập trình viên xác định hành động thay thế khi điều kiện không đúng. Câu lệnh "else" thường đi kèm với câu lệnh "if" và có thể kết hợp với câu lệnh "elsif" để kiểm tra nhiều điều kiện khác nhau.

### Cú Pháp
```ruby
if điều_kiện
  # Khối mã thực thi nếu điều kiện đúng
else
  # Khối mã thực thi nếu điều kiện sai
end
```

### Mô Tả
- **Điều kiện**: Là biểu thức logic mà bạn muốn kiểm tra. Nếu điều kiện này trả về `true`, khối mã sau câu lệnh "if" sẽ được thực thi.
- **Khối mã "else"**: Nếu điều kiện trả về `false`, khối mã trong câu lệnh "else" sẽ được thực thi.

## Ví Dụ
### Ví Dụ Cơ Bản
```ruby
tuoi = 18

if tuoi >= 18
  puts "Bạn đủ tuổi để lái xe."
else
  puts "Bạn chưa đủ tuổi để lái xe."
end
```
*Output*: "Bạn đủ tuổi để lái xe."

### Ví Dụ Với "elsif"
```ruby
diem = 75

if diem >= 90
  puts "Xuất sắc"
elsif diem >= 75
  puts "Khá"
else
  puts "Cần cải thiện"
end
```
*Output*: "Khá"

## Giải Thích
Mặc dù câu lệnh "else" rất hữu ích trong việc kiểm soát luồng chương trình, nhưng có một số điều cần lưu ý:
- **Không có điều kiện**: Câu lệnh "else" không cần điều kiện nào. Nó sẽ được thực thi khi tất cả các điều kiện trước đó đều không đúng.
- **Chỉ một khối mã**: Bạn chỉ có thể có một khối mã "else" cho mỗi câu lệnh "if". Nếu bạn cần kiểm tra nhiều điều kiện, hãy sử dụng "elsif".

## Tóm Tắt Một Dòng
Câu lệnh "else" trong Ruby cho phép thực thi khối mã thay thế khi điều kiện trong câu lệnh "if" không được thỏa mãn.