<!--
Meta Description: # Tìm Hiểu Về "defined?" Trong Ruby: Cách Kiểm Tra Biến Có Được Định Nghĩa Hay Không ## Tóm tắt `defined?` là một từ khóa trong Ruby cho phép lập trìn...
Meta Keywords: defined, một, kiểm, tra, được
-->

# Tìm Hiểu Về "defined?" Trong Ruby: Cách Kiểm Tra Biến Có Được Định Nghĩa Hay Không

## Tóm tắt
`defined?` là một từ khóa trong Ruby cho phép lập trình viên kiểm tra xem một biến, phương thức, hoặc một hằng số có được định nghĩa hay không. Đây là một công cụ hữu ích trong việc kiểm tra sự tồn tại của các đối tượng trong mã nguồn.

## Tài liệu
### Mục đích
`defined?` được sử dụng để xác định trạng thái của một biến, phương thức, hoặc hằng số. Nếu đối tượng được kiểm tra đã được định nghĩa, `defined?` sẽ trả về một chuỗi mô tả loại đối tượng đó. Nếu không, nó sẽ trả về `nil`.

### Cách sử dụng
Cú pháp của `defined?` rất đơn giản. Bạn chỉ cần sử dụng từ khóa này theo sau là biến hoặc phương thức mà bạn muốn kiểm tra.

```ruby
defined?(toán_tử)
```

### Chi tiết
- Trả về `nil` nếu đối tượng không tồn tại.
- Trả về một chuỗi mô tả nếu đối tượng đã được định nghĩa. Ví dụ: 
  - `"local-variable"` cho biến cục bộ.
  - `"method"` cho phương thức.
  - `"constant"` cho hằng số.

## Ví dụ
1. Kiểm tra biến cục bộ:
   ```ruby
   x = 10
   puts defined?(x) # => "local-variable"
   ```

2. Kiểm tra biến chưa được định nghĩa:
   ```ruby
   puts defined?(y) # => nil
   ```

3. Kiểm tra phương thức:
   ```ruby
   def hello
     "Xin chào!"
   end

   puts defined?(hello) # => "method"
   ```

4. Kiểm tra hằng số:
   ```ruby
   PI = 3.14
   puts defined?(PI) # => "constant"
   ```

## Giải thích
- **Cảnh giác với biến chưa được định nghĩa**: Việc sử dụng `defined?` để kiểm tra một biến chưa được định nghĩa sẽ không gây ra lỗi, nhưng sẽ trả về `nil`, điều này có thể gây nhầm lẫn nếu bạn không chú ý.
- **Khác biệt với `nil?`**: `defined?` khác với phương thức `nil?`. `defined?` kiểm tra sự tồn tại của đối tượng, trong khi `nil?` chỉ kiểm tra xem một đối tượng có phải là `nil` hay không.
- **Không dùng trong biểu thức**: `defined?` không thể được sử dụng trong một biểu thức như một phần của một dòng mã khác.

## Tóm tắt một dòng
`defined?` là từ khóa trong Ruby dùng để kiểm tra xem một biến, phương thức, hoặc hằng số có được định nghĩa hay không, trả về chuỗi mô tả hoặc `nil`.