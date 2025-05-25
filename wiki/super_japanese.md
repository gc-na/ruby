<!--
Meta Description: # Rubyにおける「super」キーワードの完全ガイド ## 概要 Rubyの「super」キーワードは、親クラスのメソッドを呼び出すために使用されます。これにより、クラスの継承関係においてメソッドのオーバーライドや拡張を行うことができます。 ## ドキュメンテーション 「super」は、子クラス...
Meta Keywords: super, end, class, def, car
-->

# Rubyにおける「super」キーワードの完全ガイド

## 概要
Rubyの「super」キーワードは、親クラスのメソッドを呼び出すために使用されます。これにより、クラスの継承関係においてメソッドのオーバーライドや拡張を行うことができます。

## ドキュメンテーション
「super」は、子クラスで定義されたメソッドから、同名のメソッドを親クラスから呼び出すための手段です。主に、以下の目的で使用されます。

- **親メソッドの呼び出し**: 子クラスでオーバーライドしたメソッド内から、親クラスの実装を再利用する。
- **引数の引き継ぎ**: `super`を使うことで、引数をそのまま親メソッドに渡すことができます。

### 使用方法
```ruby
class Parent
  def greet(name)
    "Hello, #{name} from Parent!"
  end
end

class Child < Parent
  def greet(name)
    super(name) + " And hello from Child!"
  end
end
```

この例では、`Child#greet`メソッドは、引数`name`を使って`Parent#greet`メソッドを呼び出しています。

## 例
以下に「super」の基本的な使用例を示します。

### 親メソッドの呼び出し
```ruby
class Animal
  def speak
    "Animal sound"
  end
end

class Dog < Animal
  def speak
    super + " Woof!"
  end
end

dog = Dog.new
puts dog.speak  # 出力: "Animal sound Woof!"
```

### 引数を渡す
```ruby
class Vehicle
  def describe(type)
    "This is a #{type}."
  end
end

class Car < Vehicle
  def describe(type)
    super(type) + " It's a fast one."
  end
end

car = Car.new
puts car.describe("car")  # 出力: "This is a car. It's a fast one."
```

## 説明
「super」を使用する際に注意すべきポイント：

- **引数の扱い**: 引数を指定しない場合、`super`は呼び出し元の引数をそのまま親メソッドに渡します。引数を指定することもでき、その場合は指定した引数が親メソッドに渡されます。
- **メソッドの存在**: 親クラスに同名のメソッドが存在しない場合、`super`を呼び出すと`NoMethodError`が発生します。このため、親メソッドが存在するか確認することが重要です。

## 一文の要約
Rubyの「super」は、子クラスから親クラスのメソッドを呼び出すための強力な機能です。