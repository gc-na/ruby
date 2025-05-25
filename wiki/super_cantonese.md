<!--
Meta Description: # Ruby 中的 super 指令：功能與用法詳解 ## 概述 在 Ruby 編程語言中，`super` 是一個關鍵字，用於在子類別中調用父類別的方法。這個功能能夠促進代碼的重用，並讓開發者能夠在子類別中擴展或修改父類別的行為。 ## 文檔 ### 目的 `super` 的主要目的是允許子類別調用...
Meta Keywords: super, ruby, name, end, child
-->

# Ruby 中的 super 指令：功能與用法詳解

## 概述
在 Ruby 編程語言中，`super` 是一個關鍵字，用於在子類別中調用父類別的方法。這個功能能夠促進代碼的重用，並讓開發者能夠在子類別中擴展或修改父類別的行為。

## 文檔
### 目的
`super` 的主要目的是允許子類別調用父類別的方法，從而可以在維持父類別功能的同時添加擴展或不同的行為。

### 用法
在 Ruby 中，`super` 可以單獨使用，也可以帶上參數。當不帶參數時，它會傳遞所有的參數給父類別的方法；當帶上參數時，則只傳遞指定的參數。

### 詳細說明
- **無參數的 `super`**：如果你在子類別的方法中使用 `super` 而不帶任何參數，Ruby 會將當前方法接收到的所有參數傳遞給父類別的方法。
- **有參數的 `super`**：如果你希望只傳遞特定的參數給父類別的方法，可以在 `super` 中指定這些參數。
- **使用 `super` 的場景**：通常在重寫父類別的方法時，若希望保留父類別的行為，可以在子類別的方法中調用 `super`。

## 範例
```ruby
class Parent
  def greet(name)
    "Hello, #{name}!"
  end
end

class Child < Parent
  def greet(name)
    super(name) + " How are you?"
  end
end

child = Child.new
puts child.greet("Alice")  # 輸出: Hello, Alice! How are you?
```

## 解釋
- **常見陷阱**：確保在使用 `super` 時，父類別中確實存在對應的方法。如果父類別中沒有該方法，會引發 `NoMethodError`。
- **參數傳遞**：當使用 `super` 時，若父類別的方法和子類別的方法參數數量不一致，可能會導致意外的行為，需特別注意。
- **尋找方法**：當調用 `super` 時，Ruby 會在父類別中尋找對應的方法。若存在多重繼承，Ruby 會遵循其方法解析順序 (Method Resolution Order, MRO)。

## 總結
`super` 是 Ruby 中一個強大的功能，允許開發者在子類別中靈活地調用父類別的方法，從而促進代碼的重用和擴展。