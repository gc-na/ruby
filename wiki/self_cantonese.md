<!--
Meta Description: # Ruby中的"self"：關鍵字的深入解析 ## 摘要 在Ruby編程中，"self"是一個特殊的關鍵字，用於指代當前對象。它在方法定義、類定義以及模塊中扮演著重要的角色，幫助開發者管理對象的上下文。 ## 文檔 "self"是一個非常有用的關鍵字，主要用於獲取當前對象的引用。當你在一個方法內部...
Meta Keywords: self, end, name, def, ruby
-->

# Ruby中的"self"：關鍵字的深入解析

## 摘要
在Ruby編程中，"self"是一個特殊的關鍵字，用於指代當前對象。它在方法定義、類定義以及模塊中扮演著重要的角色，幫助開發者管理對象的上下文。

## 文檔
"self"是一個非常有用的關鍵字，主要用於獲取當前對象的引用。當你在一個方法內部使用"self"，它會返回當前調用該方法的對象。在類和模塊中，"self"可以用來定義類方法和模塊方法，這些方法與實例方法不同，後者是針對對象實例的。

### 用法：
- **在實例方法中**，"self"代表當前實例。
- **在類方法中**，"self"代表當前類。
- **在模塊中**，"self"代表當前模塊。

### 詳細說明：
1. **實例方法中的"self"**：
   在實例方法裡，"self"用來訪問對象的屬性和其他方法。
   
   ```ruby
   class Dog
     attr_accessor :name

     def initialize(name)
       @name = name
     end

     def bark
       puts "#{self.name} says woof!"
     end
   end
   ```

2. **類方法中的"self"**：
   當你在類中定義類方法時，"self"用於調用該類內的方法。
   
   ```ruby
   class Dog
     def self.species
       "Canine"
     end
   end
   ```

3. **模塊中的"self"**：
   在模塊中，"self"用於定義模塊方法。
   
   ```ruby
   module Animal
     def self.sound
       "Generic animal sound"
     end
   end
   ```

## 範例
以下是"self"的基本用法範例：

```ruby
class Cat
  attr_accessor :name

  def initialize(name)
    @name = name
  end

  def meow
    puts "#{self.name} says meow!"
  end

  def self.species
    "Feline"
  end
end

whiskers = Cat.new("Whiskers")
whiskers.meow        # 輸出: Whiskers says meow!
puts Cat.species     # 輸出: Feline
```

## 解釋
使用"self"時，開發者可能會遇到一些常見的問題：
- **上下文混淆**：在不同的上下文中，"self"的含義會改變，必須確保在正確的上下文中使用。
- **類方法與實例方法的區別**：在類方法中，"self"不會指向實例，因此不能使用實例變量。

## 一句話總結
"self"是Ruby中的一個關鍵字，用於指代當前對象，幫助開發者在實例方法和類方法中進行上下文管理。