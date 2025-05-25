<!--
Meta Description: # Từ Khóa "return" trong Ruby: Hướng Dẫn Chi Tiết và Ví Dụ ## Tóm Tắt Từ khóa `return` trong Ruby được sử dụng để thoát khỏi một phương thức và trả về...
Meta Keywords: return, thức, phương, trả, trong
-->

# Từ Khóa "return" trong Ruby: Hướng Dẫn Chi Tiết và Ví Dụ

## Tóm Tắt
Từ khóa `return` trong Ruby được sử dụng để thoát khỏi một phương thức và trả về giá trị cho nơi gọi phương thức đó. Đây là một thành phần quan trọng giúp kiểm soát luồng thực thi trong các chương trình Ruby.

## Tài Liệu
### Mục Đích
`return` cho phép bạn trả về giá trị từ một phương thức. Khi gặp từ khóa này, Ruby sẽ ngừng thực thi phương thức hiện tại và trả về giá trị đã chỉ định.

### Cách Sử Dụng
Cú pháp cơ bản của `return` như sau:
```ruby
def ten_phuong_thuc
  return gia_tri
end
```
- `gia_tri` có thể là bất kỳ biểu thức nào mà bạn muốn trả về từ phương thức.

### Chi Tiết
- Nếu không có giá trị nào được chỉ định cho `return`, phương thức sẽ trả về `nil` mặc định.
- Bạn có thể sử dụng `return` ở bất kỳ đâu trong thân phương thức.
- Nếu một phương thức không có `return`, giá trị của biểu thức cuối cùng được thực thi trong phương thức sẽ được tự động trả về.

## Ví Dụ
### Ví Dụ Cơ Bản
```ruby
def tinh_tong(a, b)
  return a + b
end

puts tinh_tong(5, 3) # Kết quả: 8
```

### Ví Dụ Không Có Giá Trị Trả Về
```ruby
def khong_co_return
  10 * 5
end

puts khong_co_return # Kết quả: 50
```

### Ví Dụ Về Việc Dùng Nhiều Lần
```ruby
def kiem_tra_so(a)
  return "Số âm" if a < 0
  return "Số không" if a == 0
  return "Số dương"
end

puts kiem_tra_so(-1) # Kết quả: Số âm
puts kiem_tra_so(0)  # Kết quả: Số không
puts kiem_tra_so(1)  # Kết quả: Số dương
```

## Giải Thích
- **Cái Bẫy Thường Gặp**: Một số lập trình viên mới có thể quên sử dụng `return` khi muốn trả về giá trị từ một phương thức. Điều này có thể dẫn đến việc phương thức trả về `nil`, gây ra lỗi không mong muốn trong mã.
- **Sử Dụng Trong Block**: Khi bạn sử dụng `return` trong một block, nó sẽ làm cho mã thoát khỏi phương thức bao quanh, không chỉ block hiện tại.

## Tóm Tắt Một Dòng
`return` trong Ruby là từ khóa dùng để trả về giá trị từ một phương thức và kiểm soát luồng thực thi của chương trình.