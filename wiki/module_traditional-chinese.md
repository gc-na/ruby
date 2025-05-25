<!--
Meta Description: # Ruby 中的模組 (Module) ## 簡介 在 Ruby 中，模組是一種用來封裝方法、類別和常數的集合。它們可以用來實現命名空間及混入功能，提供了組織程式碼的有效方式，並促進了代碼的重用。 ## 文檔 模組在 Ruby 中的主要用途包括： 1. **命名空間**：模組可以用來防止命名衝突。...
Meta Keywords: ruby, end, mymodule, hello, module
-->

# Ruby 中的模組 (Module)

## 簡介
在 Ruby 中，模組是一種用來封裝方法、類別和常數的集合。它們可以用來實現命名空間及混入功能，提供了組織程式碼的有效方式，並促進了代碼的重用。

## 文檔
模組在 Ruby 中的主要用途包括：

1. **命名空間**：模組可以用來防止命名衝突。將相關的類別和方法組織在一個模組中，可以避免與其他類別或方法的命名衝突。
   
2. **混入功能**：模組可以通過包含或擴展的方式將其方法加入到其他類別中。這種特性使得 Ruby 支持多重繼承的功能。

### 使用方法
要定義一個模組，使用 `module` 關鍵字，然後在模組中定義方法或常數。例如：

```ruby
module MyModule
  CONSTANT = 3.14

  def self.say_hello
    puts "Hello from MyModule!"
  end
end
```

要在類別中使用模組，可以使用 `include` 或 `extend`：

```ruby
class MyClass
  include MyModule  # 將模組的實例方法混入

  def greet
    say_hello  # 可以直接呼叫模組中的方法
  end
end

obj = MyClass.new
obj.greet  # 輸出: Hello from MyModule!
```

### 重要細節
- **模組不能被實例化**：與類別不同，模組無法被實例化，因此不能使用 `new` 方法。
- **命名空間**：可以使用 `::` 來訪問模組中的常數或方法，例如 `MyModule::CONSTANT`。
- **使用 `extend`**：如果希望模組的實例方法成為類別方法，可以使用 `extend`：

```ruby
class MyClass
  extend MyModule  # 將模組的類別方法混入

  def self.greet
    say_hello  # 可以直接呼叫模組中的方法
  end
end

MyClass.greet  # 輸出: Hello from MyModule!
```

## 範例
```ruby
module MathHelpers
  def self.add(a, b)
    a + b
  end
end

puts MathHelpers.add(2, 3)  # 輸出: 5
```

```ruby
module Greetings
  def self.hello(name)
    "Hello, #{name}!"
  end
end

puts Greetings.hello("Ruby")  # 輸出: Hello, Ruby!
```

## 說明
- **命名衝突**：在大型應用程序中，避免命名衝突是至關重要的。使用模組可以有效地解決這個問題。
- **性能考量**：雖然使用模組可以提高代碼的可讀性和可維護性，但過度使用可能會影響性能，特別是在深度嵌套的情況下。
- **混入時的注意**：確保在混入模組時不會覆蓋已有的方法，這可能會導致意想不到的行為。

## 總結
模組是 Ruby 中的一個強大特性，用於組織程式碼、實現命名空間和提供混入功能。