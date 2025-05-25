<!--
Meta Description: # Từ Khóa "then" Trong Ruby: Tính Năng Và Cách Sử Dụng ## Tóm Tắt Từ khóa "then" trong Ruby được sử dụng như một phần của cấu trúc điều kiện, cho phép...
Meta Keywords: then, dụng, trong, lệnh, ruby
-->

# Từ Khóa "then" Trong Ruby: Tính Năng Và Cách Sử Dụng

## Tóm Tắt
Từ khóa "then" trong Ruby được sử dụng như một phần của cấu trúc điều kiện, cho phép người lập trình kết hợp các câu lệnh với điều kiện trong các biểu thức `if`, `unless`, và `case`. 

## Tài Liệu
### Mục Đích
Từ khóa "then" giúp tạo ra mã lệnh rõ ràng hơn trong các biểu thức điều kiện. Nó thường được sử dụng để phân tách các điều kiện và câu lệnh thực thi, giúp mã dễ đọc hơn.

### Cách Sử Dụng
Từ khóa "then" có thể được sử dụng trong các cấu trúc điều kiện như sau:

- **Cú pháp `if`**: 
  ```ruby
  if điều_kiện then
    # câu lệnh thực thi
  end
  ```

- **Cú pháp `unless`**:
  ```ruby
  unless điều_kiện then
    # câu lệnh thực thi
  end
  ```

- **Cú pháp `case`**:
  ```ruby
  case biến
  when giá_trị1 then
    # câu lệnh thực thi
  when giá_trị2 then
    # câu lệnh thực thi
  else
    # câu lệnh thực thi
  end
  ```

### Chi Tiết
- Từ khóa "then" không bắt buộc trong Ruby, nhưng có thể làm cho mã nguồn dễ hiểu hơn, đặc biệt khi câu lệnh thực thi dài hoặc phức tạp.
- Khi sử dụng "then", bạn có thể viết mã trên cùng một dòng, điều này có thể giúp tiết kiệm không gian và tăng tính rõ ràng.

## Ví Dụ
### Ví dụ 1: Sử Dụng Trong Câu Lệnh `if`
```ruby
x = 10
if x > 5 then
  puts "X lớn hơn 5"
end
```

### Ví dụ 2: Sử Dụng Trong Câu Lệnh `unless`
```ruby
y = 3
unless y > 5 then
  puts "Y không lớn hơn 5"
end
```

### Ví dụ 3: Sử Dụng Trong Câu Lệnh `case`
```ruby
day = "Thứ Hai"
case day
when "Thứ Hai" then
  puts "Hôm nay là thứ Hai"
when "Thứ Ba" then
  puts "Hôm nay là thứ Ba"
else
  puts "Không phải thứ Hai hoặc thứ Ba"
end
```

## Giải Thích
- Một số lập trình viên có thể bỏ qua việc sử dụng "then" vì Ruby cho phép viết mã mà không cần nó. Tuy nhiên, việc sử dụng "then" có thể làm cho mã trở nên dễ hiểu hơn trong một số trường hợp.
- Một điều cần lưu ý là sử dụng "then" có thể làm cho mã trở nên dài hơn nếu không được sử dụng một cách hợp lý, vì vậy, hãy cân nhắc sử dụng nó trong những tình huống cần thiết.

## Tóm Tắt Một Dòng
Từ khóa "then" trong Ruby giúp cải thiện độ rõ ràng của cấu trúc điều kiện trong mã nguồn.