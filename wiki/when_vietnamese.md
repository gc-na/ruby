<!--
Meta Description: # Khi nào sử dụng "when" trong Ruby: Hướng dẫn chi tiết ## Tóm tắt Câu lệnh `when` trong Ruby được sử dụng trong cấu trúc điều kiện `case`, cho phép k...
Meta Keywords: when, trong, một, kiểm, tra
-->

# Khi nào sử dụng "when" trong Ruby: Hướng dẫn chi tiết

## Tóm tắt
Câu lệnh `when` trong Ruby được sử dụng trong cấu trúc điều kiện `case`, cho phép kiểm tra nhiều điều kiện khác nhau một cách hiệu quả và rõ ràng.

## Tài liệu
Câu lệnh `when` trong Ruby là một phần của cấu trúc điều kiện `case`, giúp lập trình viên so sánh giá trị của một biến với nhiều giá trị khác nhau. Nó rất hữu ích khi bạn cần kiểm tra nhiều trường hợp khác nhau mà không phải sử dụng nhiều câu lệnh `if...elsif`.

Cú pháp cơ bản của cấu trúc `case` với `when` là như sau:

```ruby
case variable
when value1
  # do something for value1
when value2
  # do something for value2
else
  # do something if no matches
end
```

Trong đó:
- `variable` là biến mà bạn muốn kiểm tra.
- `value1`, `value2`,... là các giá trị mà bạn muốn so sánh với `variable`.
- `else` là phần tùy chọn có thể giúp xử lý trường hợp không có giá trị nào khớp.

## Ví dụ
Dưới đây là một số ví dụ minh họa cho việc sử dụng `when` trong Ruby:

### Ví dụ 1: Kiểm tra ngày trong tuần
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

### Ví dụ 2: Kiểm tra điểm số
```ruby
score = 85

case score
when 90..100
  puts "Xuất sắc!"
when 75..89
  puts "Khá!"
when 60..74
  puts "Trung bình!"
else
  puts "Cần cải thiện!"
end
```

## Giải thích
Khi sử dụng `when`, có một số điểm cần lưu ý:
- **Trật tự kiểm tra**: `when` sẽ kiểm tra các điều kiện theo thứ tự từ trên xuống dưới, do đó, thứ tự các câu lệnh `when` có thể ảnh hưởng đến kết quả.
- **Sử dụng dấu `..` để chỉ khoảng**: Bạn có thể sử dụng dấu `..` để chỉ một khoảng giá trị, giúp đơn giản hóa việc kiểm tra nhiều giá trị liên tiếp.
- **Không trả về giá trị**: Câu lệnh `case` không trả về giá trị như một số ngôn ngữ khác, vì vậy không nên cố gắng gán giá trị cho nó.

## Tóm tắt một dòng
Câu lệnh `when` trong Ruby giúp kiểm tra nhiều điều kiện khác nhau một cách hiệu quả trong cấu trúc điều kiện `case`.