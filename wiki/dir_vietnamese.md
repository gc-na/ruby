<!--
Meta Description: # Tìm Hiểu Về Lớp Dir Trong Ruby: Quản Lý Thư Mục Dễ Dàng ## Tóm Tắt Lớp `Dir` trong Ruby cung cấp các phương thức để làm việc với thư mục và tệp tin,...
Meta Keywords: mục, thư, dir, tệp, trong
-->

# Tìm Hiểu Về Lớp Dir Trong Ruby: Quản Lý Thư Mục Dễ Dàng

## Tóm Tắt
Lớp `Dir` trong Ruby cung cấp các phương thức để làm việc với thư mục và tệp tin, cho phép bạn liệt kê, tạo, và xóa thư mục một cách hiệu quả.

## Tài Liệu
### Mục Đích
Lớp `Dir` trong Ruby được thiết kế để tương tác với hệ thống tệp, cho phép bạn thực hiện các thao tác như tạo thư mục, xóa thư mục, và đọc danh sách tệp trong một thư mục cụ thể.

### Cách Sử Dụng
Để sử dụng lớp `Dir`, bạn có thể gọi các phương thức của nó mà không cần khởi tạo một đối tượng cụ thể. Dưới đây là một số phương thức phổ biến:

- **`Dir.pwd`**: Trả về đường dẫn của thư mục hiện tại.
- **`Dir.entries(path)`**: Trả về một mảng chứa tên của tất cả các tệp và thư mục trong thư mục được chỉ định.
- **`Dir.mkdir(path)`**: Tạo một thư mục mới tại vị trí được chỉ định.
- **`Dir.rmdir(path)`**: Xóa thư mục trống tại vị trí được chỉ định.

### Chi Tiết
Lớp `Dir` rất hữu ích khi bạn cần quản lý các thư mục và tệp tin trong ứng dụng Ruby của mình. Bạn có thể dễ dàng lấy danh sách các tệp trong một thư mục, kiểm tra thư mục hiện tại, và thay đổi thư mục làm việc.

## Ví Dụ
```ruby
# Lấy đường dẫn thư mục hiện tại
puts "Thư mục hiện tại: #{Dir.pwd}"

# Liệt kê các tệp trong thư mục hiện tại
puts "Danh sách tệp trong thư mục hiện tại:"
Dir.entries('.').each { |file| puts file }

# Tạo thư mục mới
Dir.mkdir('thu_muc_moi') unless Dir.exist?('thu_muc_moi')

# Xóa thư mục trống
Dir.rmdir('thu_muc_moi') if Dir.exist?('thu_muc_moi')
```

## Giải Thích
Khi sử dụng lớp `Dir`, bạn cần lưu ý rằng:
- Phương thức `Dir.rmdir` chỉ có thể xóa thư mục trống. Nếu thư mục chứa tệp, bạn sẽ gặp lỗi.
- Để tránh lỗi khi tạo thư mục đã tồn tại, bạn có thể kiểm tra sự tồn tại của thư mục bằng `Dir.exist?` trước khi tạo.
- Lớp `Dir` hoạt động trên các hệ điều hành khác nhau, nhưng đường dẫn tệp có thể thay đổi theo từng hệ điều hành.

## Tóm Tắt Một Dòng
Lớp `Dir` trong Ruby cung cấp các phương thức mạnh mẽ để quản lý thư mục và tệp tin, giúp bạn dễ dàng thực hiện các thao tác liên quan đến hệ thống tệp.