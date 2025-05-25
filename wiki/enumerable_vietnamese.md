<!--
Meta Description: # Enumerable trong Ruby: Hướng Dẫn Chi Tiết và Ví Dụ Cụ Thể ## Tóm tắt Enumerable là một module trong Ruby cung cấp các phương thức để làm việc với cá...
Meta Keywords: các, một, phương, thức, dụng
-->

# Enumerable trong Ruby: Hướng Dẫn Chi Tiết và Ví Dụ Cụ Thể

## Tóm tắt
Enumerable là một module trong Ruby cung cấp các phương thức để làm việc với các tập hợp như mảng và hash, cho phép lặp qua các phần tử và thực hiện các tác vụ như tìm kiếm, lọc và biến đổi.

## Tài liệu
### Mục đích
Module Enumerable cung cấp các phương thức để thực hiện các thao tác lặp lại trên các đối tượng như Array và Hash. Nó cho phép bạn tận dụng sức mạnh của phương thức `each`, đồng thời cung cấp nhiều phương thức hữu ích khác để xử lý các tập hợp dữ liệu.

### Cách sử dụng
Để sử dụng Enumerable, một đối tượng cần bao gồm module này, thường là Array hoặc Hash. Bạn có thể gọi các phương thức như `map`, `select`, và `reduce` để xử lý dữ liệu.

### Chi tiết
- **Phương thức chính**: 
  - `each`: Lặp qua từng phần tử trong tập hợp.
  - `map`: Biến đổi mỗi phần tử và trả về một mảng mới.
  - `select`: Lọc các phần tử dựa trên điều kiện cho trước.
  - `reject`: Ngược lại với `select`, loại bỏ các phần tử không thỏa mãn điều kiện.
  - `reduce`: Kết hợp các phần tử lại với nhau thành một giá trị duy nhất.

## Ví dụ
### Sử dụng `each`
```ruby
[1, 2, 3].each do |number|
  puts number
end
```

### Sử dụng `map`
```ruby
squared = [1, 2, 3].map { |number| number ** 2 }
puts squared.inspect # => [1, 4, 9]
```

### Sử dụng `select`
```ruby
evens = [1, 2, 3, 4].select { |number| number.even? }
puts evens.inspect # => [2, 4]
```

### Sử dụng `reduce`
```ruby
sum = [1, 2, 3].reduce(0) { |acc, number| acc + number }
puts sum # => 6
```

## Giải thích
- **Cạm bẫy phổ biến**: Một số lập trình viên mới có thể gặp khó khăn khi sử dụng phương thức `reduce` vì nó yêu cầu một giá trị khởi tạo. Nếu không cung cấp, nó sẽ sử dụng phần tử đầu tiên của mảng làm giá trị khởi tạo.
- **Hiệu suất**: Khi làm việc với tập hợp lớn, hãy cẩn thận với các phương thức như `map` và `select`, vì chúng tạo ra các mảng mới và có thể tiêu tốn nhiều bộ nhớ.

## Tóm tắt một dòng
Enumerable là một module trong Ruby cho phép bạn lặp qua và xử lý các tập hợp dữ liệu một cách hiệu quả thông qua các phương thức mạnh mẽ.