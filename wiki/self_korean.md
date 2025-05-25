<!--
Meta Description: # Ruby의 self: 객체 지향 프로그래밍의 핵심 ## 개요 Ruby에서 `self`는 현재 객체를 참조하는 특별한 키워드로, 메소드, 클래스, 모듈 등에서 사용됩니다. 이는 객체 지향 프로그래밍의 중요한 개념으로, 코드의 맥락을 이해하는 데 필수적입니다. ## 문...
Meta Keywords: self, 클래스, end, 메소드, 인스턴스
-->

# Ruby의 self: 객체 지향 프로그래밍의 핵심

## 개요
Ruby에서 `self`는 현재 객체를 참조하는 특별한 키워드로, 메소드, 클래스, 모듈 등에서 사용됩니다. 이는 객체 지향 프로그래밍의 중요한 개념으로, 코드의 맥락을 이해하는 데 필수적입니다.

## 문서화
`self`는 Ruby에서 현재 객체를 나타내며, 메소드 안에서 호출될 때 해당 메소드를 소속한 객체를 가리킵니다. 클래스 정의 내에서는 클래스 자체를, 인스턴스 메소드 내에서는 인스턴스를 참조합니다. 예를 들어, 인스턴스 메소드에서 `self`를 사용하면 그 메소드를 호출한 객체를 반환합니다. 클래스 메소드 내에서 `self`는 클래스 자체를 참조합니다.

### 사용법
`self`는 다음과 같은 상황에서 사용됩니다:
- 인스턴스 메소드 내: 메소드가 호출된 인스턴스를 참조합니다.
- 클래스 메소드 내: 메소드를 정의하는 클래스 자체를 참조합니다.
- 클래스 정의 내: 클래스의 변수 및 메소드를 정의할 때 사용됩니다.

## 예제
### 인스턴스 메소드에서의 사용
```ruby
class Dog
  def bark
    puts "Woof! My name is #{self.name}"
  end

  def name
    "Rex"
  end
end

dog = Dog.new
dog.bark  # 출력: Woof! My name is Rex
```

### 클래스 메소드에서의 사용
```ruby
class Cat
  def self.meow
    puts "Meow! I am a cat."
  end
end

Cat.meow  # 출력: Meow! I am a cat.
```

### 클래스 변수와의 관계
```ruby
class Animal
  @@species = "Mammal"

  def self.species
    @@species
  end

  def self.show_species
    puts "This is a #{self.species}."
  end
end

Animal.show_species  # 출력: This is a Mammal.
```

## 설명
`self`를 사용할 때 주의해야 할 몇 가지 사항이 있습니다:
- `self`는 메소드가 호출되는 문맥에 따라 다르게 해석됩니다. 따라서 메소드의 정의 위치에 따라 `self`가 무엇을 참조하는지 이해하는 것이 중요합니다.
- 인스턴스 메소드에서 `self`는 인스턴스 객체를 가리키지만, 클래스 메소드에서 `self`는 클래스 자체를 가리킵니다.
- `self`를 잘못 사용하면 예기치 않은 결과를 초래할 수 있으므로, 메소드 내에서의 맥락을 항상 고려해야 합니다.

## 한 줄 요약
Ruby의 `self`는 현재 객체를 참조하는 키워드로, 인스턴스 및 클래스 메소드에서 중요한 역할을 합니다.