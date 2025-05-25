<!--
Meta Description: # Lệnh "p" trong Ruby: Hiểu Biết Cơ Bản và Cách Sử Dụng ## Tóm tắt Lệnh `p` trong Ruby được sử dụng để in ra giá trị của một biểu thức hoặc đối tượng,...
Meta Keywords: trong, một, giá, trị, ruby
-->

# Lệnh "p" trong Ruby: Hiểu Biết Cơ Bản và Cách Sử Dụng

## Tóm tắt
Lệnh `p` trong Ruby được sử dụng để in ra giá trị của một biểu thức hoặc đối tượng, đồng thời hiển thị giá trị đó theo định dạng dễ đọc cho người phát triển.

## Tài liệu
Lệnh `p` trong Ruby là một phương thức trong lớp `Kernel`, cho phép bạn in ra giá trị của một đối tượng lên màn hình. Nó hữu ích cho việc gỡ lỗi, vì nó không chỉ in ra giá trị mà còn trả về giá trị của biểu thức đó, giúp lập trình viên dễ dàng kiểm tra giá trị của các biến hoặc đối tượng trong quá trình phát triển ứng dụng.

### Cú pháp
```ruby
p(obj)
```

### Tham số
- `obj`: Đối tượng hoặc biểu thức mà bạn muốn in ra.

### Trả về
`p` trả về giá trị của đối tượng được truyền vào.

## Ví dụ
Dưới đây là một số ví dụ cơ bản về cách sử dụng lệnh `p` trong Ruby:

```ruby
# Ví dụ 1: In một chuỗi
p "Hello, World!"  # Kết quả: "Hello, World!"

# Ví dụ 2: In một số nguyên
p 42  # Kết quả: 42

# Ví dụ 3: In một mảng
p [1, 2, 3, 4, 5]  # Kết quả: [1, 2, 3, 4, 5]

# Ví dụ 4: In một đối tượng phức tạp
p { name: "Ruby", version: 3.0 }  # Kết quả: {:name=>"Ruby", :version=>3.0}
```

## Giải thích
Mặc dù `p` rất hữu ích, có một số điều cần lưu ý khi sử dụng:

- **Định dạng đầu ra**: Lệnh `p` sẽ in ra giá trị của đối tượng theo cách mà lập trình viên có thể dễ dàng đọc được, bao gồm việc hiển thị cả dấu ngoặc đơn cho các đối tượng như mảng và hash.
- **Khác với `puts`**: Trong khi `puts` chỉ in giá trị mà không trả về, `p` sẽ trả về biểu thức, điều này có thể hữu ích trong một số trường hợp gỡ lỗi.
- **Không dùng trong sản phẩm**: Mặc dù `p` rất hiệu quả trong giai đoạn phát triển, bạn không nên sử dụng nó trong mã sản phẩm vì nó có thể in ra thông tin nhạy cảm hoặc không cần thiết.

## Tóm tắt một dòng
Lệnh `p` trong Ruby là một phương thức hữu ích để in ra giá trị của một đối tượng, giúp lập trình viên dễ dàng gỡ lỗi và kiểm tra giá trị trong quá trình phát triển ứng dụng.