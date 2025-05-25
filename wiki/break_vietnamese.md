<!--
Meta Description: # Câu lệnh `break` trong Ruby: Cách sử dụng và ý nghĩa ## Tóm tắt Câu lệnh `break` trong Ruby được sử dụng để thoát khỏi một vòng lặp hoặc một khối lệ...
Meta Keywords: break, lặp, vòng, lệnh, trong
-->

# Câu lệnh `break` trong Ruby: Cách sử dụng và ý nghĩa

## Tóm tắt
Câu lệnh `break` trong Ruby được sử dụng để thoát khỏi một vòng lặp hoặc một khối lệnh. Đây là một công cụ mạnh mẽ giúp kiểm soát luồng thực thi trong chương trình, cho phép bạn ngừng thực hiện khi đạt được một điều kiện nhất định.

## Tài liệu
Câu lệnh `break` cho phép lập trình viên thoát khỏi các cấu trúc lặp như `while`, `until`, `for`, hoặc `each`. Khi `break` được gọi, nó sẽ ngay lập tức dừng vòng lặp hiện tại và chuyển đến câu lệnh tiếp theo sau vòng lặp đó.

### Cách sử dụng
Cú pháp cơ bản của câu lệnh `break` là:

```ruby
break
```

Ngoài ra, bạn có thể sử dụng `break` với một giá trị để trả về giá trị đó từ phương thức hoặc khối lệnh. Ví dụ:

```ruby
result = array.each do |item|
  break item if condition_met?(item)
end
```

### Chi tiết
- **Vòng lặp `while`**: Dừng vòng lặp khi điều kiện được thỏa mãn.
  
```ruby
i = 0
while i < 10
  break if i == 5
  i += 1
end
```

- **Vòng lặp `for`**: Giống như trong `while`, `break` cũng có thể sử dụng trong vòng lặp `for`.

```ruby
for i in 0..10
  break if i > 5
  puts i
end
```

- **Khối lệnh**: Câu lệnh `break` có thể được sử dụng trong các khối lệnh như `each` để dừng lặp khi điều kiện thỏa mãn.

## Ví dụ
### Ví dụ 1: Dùng `break` trong vòng lặp `while`
```ruby
i = 0
while i < 5
  puts i
  break if i == 3
  i += 1
end
```
Kết quả: 
```
0
1
2
3
```

### Ví dụ 2: Dùng `break` trong vòng lặp `each`
```ruby
[1, 2, 3, 4, 5].each do |num|
  break if num == 3
  puts num
end
```
Kết quả:
```
1
2
```

## Giải thích
Một số điểm cần lưu ý khi sử dụng `break`:
- **Chỉ áp dụng cho vòng lặp**: `break` chỉ có tác dụng trong các cấu trúc lặp, nếu sử dụng ngoài ngữ cảnh này sẽ gây ra lỗi.
- **Giá trị trả về**: `break` có thể trả về giá trị, nhưng chỉ nếu nó được sử dụng trong một phương thức hoặc khối.
- **Nesting**: Nếu có nhiều vòng lặp lồng nhau, `break` sẽ chỉ thoát khỏi vòng lặp gần nhất.

## Tóm tắt một dòng
Câu lệnh `break` trong Ruby cho phép lập trình viên thoát khỏi vòng lặp hoặc khối lệnh khi một điều kiện nhất định được đáp ứng.