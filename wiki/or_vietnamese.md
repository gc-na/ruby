<!--
Meta Description: # Toán Tử "or" Trong Ruby: Cách Sử Dụng và Ví Dụ Thực Tế ## Tóm tắt Toán tử "or" trong Ruby là một toán tử logic, cho phép thực hiện các phép toán điề...
Meta Keywords: toán, trong, điều, ruby, kiện
-->

# Toán Tử "or" Trong Ruby: Cách Sử Dụng và Ví Dụ Thực Tế

## Tóm tắt
Toán tử "or" trong Ruby là một toán tử logic, cho phép thực hiện các phép toán điều kiện. Nó được sử dụng để kiểm tra nhiều điều kiện khác nhau và trả về giá trị đầu tiên đúng.

## Tài liệu
Toán tử "or" trong Ruby được sử dụng để kết hợp hai hoặc nhiều điều kiện. Nếu bất kỳ điều kiện nào trong số đó là đúng (truthy), toán tử sẽ trả về giá trị của điều kiện đó. Nếu tất cả các điều kiện đều sai (falsy), nó sẽ trả về giá trị của điều kiện cuối cùng. 

### Cú pháp:
```ruby
result = điều_kiện_1 or điều_kiện_2
```

### Mục đích:
Toán tử "or" thường được sử dụng trong các tình huống mà bạn cần kiểm tra nhiều điều kiện mà chỉ cần một trong số đó đúng để thực hiện hành động.

### Chi tiết:
- Toán tử "or" có độ ưu tiên thấp hơn so với nhiều toán tử khác trong Ruby, như toán tử "&&" (and). Do đó, nếu bạn sử dụng cả hai trong cùng một biểu thức, hãy cẩn thận với thứ tự thực hiện.
- Trong Ruby, giá trị `nil` và `false` được coi là "falsy", trong khi tất cả các giá trị khác đều được coi là "truthy".

## Ví dụ
### Ví dụ 1: Sử dụng toán tử "or" đơn giản
```ruby
a = nil
b = 5
result = a or b
puts result # Kết quả: 5
```

### Ví dụ 2: Kiểm tra điều kiện
```ruby
x = 10
y = 20
result = (x > 15) or (y > 15)
puts result # Kết quả: false
```

### Ví dụ 3: Sử dụng với biến
```ruby
user_input = nil
default_value = "Giá trị mặc định"
final_value = user_input or default_value
puts final_value # Kết quả: "Giá trị mặc định"
```

## Giải thích
Một số điều cần lưu ý khi sử dụng toán tử "or":
- **Độ ưu tiên**: Nếu bạn kết hợp "or" với các toán tử khác như "and", hãy sử dụng dấu ngoặc để đảm bảo thứ tự thực hiện đúng.
- **Trả về giá trị**: Toán tử "or" không chỉ trả về true/false mà còn trả về giá trị của điều kiện đầu tiên đúng.
- **Khác với "||"**: Toán tử "or" có thể được thay thế bằng toán tử "||" trong Ruby, nhưng "||" có độ ưu tiên cao hơn, dẫn đến hành vi khác nhau trong một số trường hợp.

## Tóm tắt một dòng
Toán tử "or" trong Ruby cho phép kết hợp nhiều điều kiện, trả về giá trị đầu tiên đúng hoặc giá trị cuối cùng nếu tất cả đều sai.