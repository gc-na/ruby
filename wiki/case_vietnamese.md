<!--
Meta Description: # Câu Lệnh Case trong Ruby: Hướng Dẫn Chi Tiết ## Tóm tắt Câu lệnh `case` trong Ruby cho phép lập trình viên thực hiện nhiều lựa chọn dựa trên giá trị...
Meta Keywords: lệnh, câu, case, với, trong
-->

# Câu Lệnh Case trong Ruby: Hướng Dẫn Chi Tiết

## Tóm tắt
Câu lệnh `case` trong Ruby cho phép lập trình viên thực hiện nhiều lựa chọn dựa trên giá trị của một biểu thức, cung cấp cách tiếp cận sạch sẽ và dễ hiểu để xử lý điều kiện.

## Tài liệu
Câu lệnh `case` trong Ruby là một công cụ mạnh mẽ cho việc kiểm tra một giá trị và thực hiện các hành động khác nhau tùy thuộc vào giá trị đó. Nó tương tự như câu lệnh `switch` trong các ngôn ngữ lập trình khác. Câu lệnh này giúp mã trở nên dễ đọc và quản lý hơn khi có nhiều điều kiện cần kiểm tra.

**Cú pháp:**
```ruby
case điều_kiện
when giá_trị_1
  # Khối lệnh nếu điều kiện khớp với giá_trị_1
when giá_trị_2
  # Khối lệnh nếu điều kiện khớp với giá_trị_2
else
  # Khối lệnh nếu không khớp với bất kỳ giá trị nào
end
```

### Mục đích
Câu lệnh `case` được sử dụng để so sánh một giá trị với nhiều lựa chọn khác nhau, giúp tiết kiệm mã và giảm thiểu lỗi so với việc sử dụng nhiều câu lệnh `if`.

## Ví dụ
### Ví dụ 1: Sử dụng cơ bản
```ruby
day = "Thứ Hai"

case day
when "Thứ Hai"
  puts "Hôm nay là đầu tuần."
when "Thứ Sáu"
  puts "Hôm nay là cuối tuần."
else
  puts "Hôm nay là một ngày trong tuần."
end
```
**Kết quả:**
```
Hôm nay là đầu tuần.
```

### Ví dụ 2: Sử dụng với biểu thức
```ruby
number = 2

case number
when 1, 2, 3
  puts "Số nằm trong khoảng 1 đến 3."
when 4..6
  puts "Số nằm trong khoảng 4 đến 6."
else
  puts "Số lớn hơn 6."
end
```
**Kết quả:**
```
Số nằm trong khoảng 1 đến 3.
```

## Giải thích
Một số điểm cần lưu ý khi sử dụng câu lệnh `case`:
- **So sánh với `===`**: Ruby sử dụng toán tử `===` để kiểm tra sự khớp. Vì vậy, các đối tượng khác nhau có thể hoạt động khác nhau với câu lệnh `case`.
- **Không bỏ qua `else`**: Nếu không có bất kỳ điều kiện nào khớp và không có `else`, chương trình sẽ không làm gì cả.
- **Tính linh hoạt**: Câu lệnh `case` có thể so sánh không chỉ với giá trị mà còn với các biểu thức phức tạp.

## Tóm tắt một dòng
Câu lệnh `case` trong Ruby cho phép lập trình viên thực hiện nhiều lựa chọn dựa trên giá trị của một biểu thức, giúp mã dễ đọc và quản lý hơn.