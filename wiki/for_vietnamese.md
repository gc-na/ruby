<!--
Meta Description: # Câu Lệnh "for" trong Ruby: Hướng Dẫn Chi Tiết ## Tóm Tắt Câu lệnh "for" trong Ruby được sử dụng để lặp qua các phần tử trong một tập hợp, như mảng h...
Meta Keywords: trong, một, câu, lệnh, lặp
-->

# Câu Lệnh "for" trong Ruby: Hướng Dẫn Chi Tiết

## Tóm Tắt
Câu lệnh "for" trong Ruby được sử dụng để lặp qua các phần tử trong một tập hợp, như mảng hoặc dãy số, giúp lập trình viên thực hiện các thao tác trên từng phần tử một cách dễ dàng và hiệu quả.

## Tài Liệu
Câu lệnh "for" trong Ruby cho phép bạn lặp qua các phần tử của một tập hợp. Cú pháp cơ bản của câu lệnh "for" như sau:

```ruby
for biến in tập_hợp
  # Lệnh thực hiện cho mỗi phần tử
end
```

### Mục Đích
Mục đích chính của câu lệnh "for" là để duyệt qua từng phần tử trong một tập hợp và thực hiện một hoặc nhiều thao tác trên từng phần tử đó.

### Cách Sử Dụng
- **Tập hợp**: Có thể là mảng, dãy số, hoặc bất kỳ đối tượng nào có thể lặp lại.
- **Biến**: Là biến tạm thời sẽ chứa giá trị của từng phần tử khi lặp.

### Chi Tiết
Câu lệnh "for" trong Ruby hoạt động tương tự như các vòng lặp khác, nhưng với cú pháp ngắn gọn và dễ hiểu hơn. Đây là một trong những cách đơn giản nhất để xử lý dữ liệu trong mảng hoặc danh sách.

## Ví Dụ
Dưới đây là một số ví dụ cơ bản về cách sử dụng câu lệnh "for":

### Ví dụ 1: Lặp qua mảng
```ruby
mang = [1, 2, 3, 4, 5]
for so in mang
  puts so
end
```
Kết quả:
```
1
2
3
4
5
```

### Ví dụ 2: Lặp qua dãy số
```ruby
for i in 1..5
  puts "Số: #{i}"
end
```
Kết quả:
```
Số: 1
Số: 2
Số: 3
Số: 4
Số: 5
```

### Ví dụ 3: Lặp qua chuỗi
```ruby
chuoi = "Ruby"
for ky_tu in chuoi.chars
  puts ky_tu
end
```
Kết quả:
```
R
u
b
y
```

## Giải Thích
Một số điểm cần lưu ý khi sử dụng câu lệnh "for":
- **Biến tạm thời**: Biến được sử dụng trong câu lệnh "for" chỉ tồn tại trong phạm vi của vòng lặp.
- **Phạm vi**: Nếu bạn cần truy cập biến ngoài vòng lặp, hãy chắc chắn nó được khai báo bên ngoài. 
- **Hiệu suất**: Trong một số trường hợp, việc sử dụng `each` với mảng có thể hiệu quả hơn so với câu lệnh "for", nhưng "for" vẫn là một lựa chọn hợp lý trong nhiều tình huống.

## Tóm Tắt Một Câu
Câu lệnh "for" trong Ruby là một công cụ mạnh mẽ để lặp qua các phần tử trong tập hợp một cách dễ dàng và trực quan.