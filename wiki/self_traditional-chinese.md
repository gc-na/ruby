<!--
Meta Description: # Ruby 中的 self：理解 Ruby 中的自我指向 ## 概述 在 Ruby 中，`self` 是一個特殊的關鍵字，用於引用當前物件的實例。無論是在類別、模組或方法內部，`self` 可以幫助開發者獲取當前上下文的物件，從而實現更靈活的程式設計。 ## 文檔 ### 目的 `self` 的主...
Meta Keywords: self, ruby, name, def, dog
-->

# Ruby 中的 self：理解 Ruby 中的自我指向

## 概述
在 Ruby 中，`self` 是一個特殊的關鍵字，用於引用當前物件的實例。無論是在類別、模組或方法內部，`self` 可以幫助開發者獲取當前上下文的物件，從而實現更靈活的程式設計。

## 文檔
### 目的
`self` 的主要目的在於提供對當前上下文的參考，無論是在物件方法還是類別方法中。這使得在方法內部訪問或改變當前物件的狀態變得簡單直觀。

### 使用
在 Ruby 中，`self` 的使用場景包括但不限於：
- 在實例方法中，`self` 代表當前的物件實例。
- 在類別方法中，`self` 代表該類別本身。
- 在類別定義中，`self` 可以用來定義類別方法。

### 詳細說明
- 在物件方法中，`self` 指向調用該方法的實例。例如，在一個類別中，若定義了 `def show` 方法，則在該方法中使用 `self` 會返回當前實例。
- 在類別方法中使用 `def self.method_name` 可以定義一個類別方法，這樣 `self` 將會指向該類別。
- 在模組中的 `self` 代表模組本身，這使得模組內的方法可以方便地被調用。

## 範例
```ruby
class Dog
  attr_accessor :name

  def initialize(name)
    @name = name
  end

  def bark
    puts "#{self.name} says woof!" # 使用 self 獲取當前實例的 name
  end

  def self.species
    "Canis lupus familiaris" # 使用 self 定義類別方法
  end
end

dog = Dog.new("Buddy")
dog.bark             # 輸出: Buddy says woof!
puts Dog.species    # 輸出: Canis lupus familiaris
```

## 解釋
- 一個常見的陷阱是將 `self` 與局部變數混淆。在方法內，`self` 將始終指向當前物件，而局部變數則是作用於其定義範圍。
- 另一个注意事项是，`self` 在不同上下文中的意義會有所不同，因此理解 `self` 在當前上下文中的行為是非常重要的。例如，在類別的類別方法中，`self` 代表類別，而在實例方法中則代表實例。

## 一句總結
`self` 是 Ruby 中的關鍵字，用於獲取當前物件的參考，無論是實例還是類別。