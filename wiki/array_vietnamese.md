<!--
Meta Description: # Mảng trong Ruby: Tất cả những gì bạn cần biết ## Tóm tắt Mảng (Array) trong Ruby là một cấu trúc dữ liệu rất mạnh mẽ cho phép lưu trữ và xử lý tập h...
Meta Keywords: mảng, ruby, một, các, phần
-->

# Mảng trong Ruby: Tất cả những gì bạn cần biết

## Tóm tắt
Mảng (Array) trong Ruby là một cấu trúc dữ liệu rất mạnh mẽ cho phép lưu trữ và xử lý tập hợp các đối tượng theo thứ tự. Mảng hỗ trợ nhiều phương thức để thao tác với các phần tử, giúp lập trình viên dễ dàng thực hiện các tác vụ khác nhau.

## Tài liệu
### Mục đích
Mảng trong Ruby được thiết kế để lưu trữ danh sách các đối tượng, cho phép bạn truy cập, thêm, sửa đổi và xóa các phần tử dễ dàng.

### Cách sử dụng
Để khai báo một mảng, bạn có thể sử dụng dấu ngoặc vuông `[]`. Ví dụ:

```ruby
fruits = ["apple", "banana", "cherry"]
```

#### Một số phương thức phổ biến:
- `push`: Thêm một phần tử vào cuối mảng.
- `pop`: Xóa và trả về phần tử cuối cùng của mảng.
- `shift`: Xóa và trả về phần tử đầu tiên của mảng.
- `unshift`: Thêm một phần tử vào đầu mảng.
- `map`: Tạo một mảng mới bằng cách áp dụng một khối lên mỗi phần tử của mảng gốc.

## Ví dụ
### Khai báo mảng
```ruby
numbers = [1, 2, 3, 4, 5]
```

### Thêm phần tử
```ruby
numbers.push(6) # numbers bây giờ là [1, 2, 3, 4, 5, 6]
```

### Xóa phần tử
```ruby
last_number = numbers.pop # last_number là 6, numbers bây giờ là [1, 2, 3, 4, 5]
```

### Duyệt qua mảng
```ruby
fruits.each do |fruit|
  puts fruit
end
```

### Sử dụng phương thức map
```ruby
squared_numbers = numbers.map { |n| n ** 2 } # squared_numbers là [1, 4, 9, 16, 25]
```

## Giải thích
Mặc dù mảng trong Ruby rất linh hoạt, có một số điều cần lưu ý:
- Mảng có thể chứa các loại đối tượng khác nhau, bao gồm cả các mảng lồng nhau.
- Thao tác trên mảng bằng cách sử dụng các phương thức có thể thay đổi nội dung mảng ban đầu nếu không có phương thức trả về mảng mới.
- Khi sử dụng `map`, bạn nên nhớ rằng nó không thay đổi mảng gốc mà trả về một mảng mới.

## Tóm tắt một dòng
Mảng trong Ruby là một cấu trúc dữ liệu linh hoạt cho phép lưu trữ và thao tác trên danh sách các đối tượng theo thứ tự.