<!--
Meta Description: # Lệnh "redo" trong Ruby: Tái thực hiện vòng lặp ## Tóm tắt Lệnh `redo` trong Ruby được sử dụng để tái thực hiện một vòng lặp mà không bắt đầu lại từ ...
Meta Keywords: lặp, vòng, giá, trị, của
-->

# Lệnh "redo" trong Ruby: Tái thực hiện vòng lặp

## Tóm tắt
Lệnh `redo` trong Ruby được sử dụng để tái thực hiện một vòng lặp mà không bắt đầu lại từ đầu. Điều này hữu ích khi bạn muốn thực hiện lại một vòng lặp với các điều kiện hiện tại mà không phải khởi tạo lại mọi thứ.

## Tài liệu
Lệnh `redo` trong Ruby cho phép bạn khôi phục lại vòng lặp mà bạn đã dừng lại do một điều kiện nào đó. Nó có thể được sử dụng bên trong các cấu trúc vòng lặp như `while`, `until`, và `for`. Lệnh này không làm thay đổi giá trị của bất kỳ biến nào và tiếp tục từ ngay sau lệnh `redo`.

### Cách sử dụng
Để sử dụng `redo`, bạn cần đặt nó trong một vòng lặp và gọi nó khi bạn muốn lặp lại lần thực hiện hiện tại. Lệnh này thường được sử dụng khi bạn cần làm gì đó lại mà không muốn khởi động lại vòng lặp.

### Cú pháp
```ruby
redo
```

## Ví dụ
### Ví dụ 1: Sử dụng trong vòng lặp `while`
```ruby
i = 0
while i < 5
  i += 1
  puts "Giá trị của i: #{i}"
  redo if i == 3 # Khi i bằng 3, sẽ tái thực hiện vòng lặp
end
```
Kết quả:
```
Giá trị của i: 1
Giá trị của i: 2
Giá trị của i: 3
Giá trị của i: 3
Giá trị của i: 4
Giá trị của i: 5
```

### Ví dụ 2: Sử dụng trong vòng lặp `for`
```ruby
for i in 1..5
  puts "Giá trị của i: #{i}"
  redo if i == 2 # Khi i bằng 2, sẽ tái thực hiện vòng lặp
end
```
Kết quả:
```
Giá trị của i: 1
Giá trị của i: 2
Giá trị của i: 2
Giá trị của i: 3
Giá trị của i: 4
Giá trị của i: 5
```

## Giải thích
Một số lưu ý khi sử dụng lệnh `redo`:
- `redo` không thay đổi giá trị của biến vòng lặp, do đó nếu bạn không cẩn thận, có thể dẫn đến vòng lặp vô hạn.
- Lệnh `redo` chỉ có thể được sử dụng bên trong các cấu trúc vòng lặp.
- Nếu bạn muốn kết thúc vòng lặp, bạn nên sử dụng lệnh `break` thay vì `redo`.

## Tóm tắt một câu
Lệnh `redo` trong Ruby cho phép bạn tái thực hiện một vòng lặp hiện tại mà không làm khởi động lại vòng lặp từ đầu.