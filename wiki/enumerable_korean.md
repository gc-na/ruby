<!--
Meta Description: # Ruby의 Enumerable 모듈: 강력한 컬렉션 조작 기능 ## 개요 Enumerable은 Ruby에서 컬렉션(배열, 해시 등)과 관련된 다양한 메서드를 제공하는 모듈로, 반복(iteration)과 집합적 연산을 간편하게 처리할 수 있게 해줍니다. 이 모듈은 객...
Meta Keywords: enumerable, 메서드를, each, 요소를, 모듈을
-->

# Ruby의 Enumerable 모듈: 강력한 컬렉션 조작 기능

## 개요
Enumerable은 Ruby에서 컬렉션(배열, 해시 등)과 관련된 다양한 메서드를 제공하는 모듈로, 반복(iteration)과 집합적 연산을 간편하게 처리할 수 있게 해줍니다. 이 모듈은 객체가 각 요소에 대해 반복할 수 있는 기능을 제공하며, 이를 통해 효율적으로 데이터 처리를 할 수 있습니다.

## 문서화

### 목적
Enumerable 모듈은 반복 가능한 객체에 대해 메서드를 제공하여, 각 요소를 순회하고, 필터링(filtering), 변환(mapping), 집계(reducing) 작업을 쉽게 수행할 수 있도록 돕습니다. 이 모듈을 포함하는 클래스는 `each` 메서드를 구현해야 하며, 이를 통해 다양한 Enumerable 메서드를 사용할 수 있습니다.

### 사용법
Enumerable 모듈을 사용하려면, 해당 모듈을 포함하려는 클래스에서 `include Enumerable`을 선언하고 `each` 메서드를 정의해야 합니다. 그러면 `map`, `select`, `reduce`와 같은 다양한 메서드를 사용할 수 있습니다.

### 세부사항
- **주요 메서드**:
  - `each`: 컬렉션의 각 요소를 순회합니다.
  - `map`: 각 요소에 주어진 블록을 적용하여 새로운 배열을 반환합니다.
  - `select`: 조건을 만족하는 요소만을 포함한 새로운 배열을 반환합니다.
  - `reduce`: 배열의 요소를 하나의 값으로 집계합니다.
  
- **예시**:
  ```ruby
  class MyCollection
    include Enumerable

    def initialize(items)
      @items = items
    end

    def each(&block)
      @items.each(&block)
    end
  end

  collection = MyCollection.new([1, 2, 3, 4, 5])
  
  # 요소를 2배로 만드는 예
  doubled = collection.map { |x| x * 2 }
  puts doubled.inspect # => [2, 4, 6, 8, 10]

  # 짝수만 선택하는 예
  evens = collection.select { |x| x.even? }
  puts evens.inspect # => [2, 4]

  # 합계를 구하는 예
  sum = collection.reduce(0) { |acc, x| acc + x }
  puts sum # => 15
  ```

## 설명
Enumerable 모듈을 사용할 때 주의해야 할 점은 `each` 메서드를 반드시 구현해야 한다는 것입니다. 이 메서드가 없으면 Enumerable의 메서드들을 사용할 수 없습니다. 또한, 블록을 사용하는 메서드들이 많기 때문에 블록의 반환값에 주의해야 합니다. 예를 들어, `select` 메서드는 블록의 결과가 true인 요소만을 포함하므로, 블록의 논리적 흐름이 올바른지 확인해야 합니다.

## 한 줄 요약
Ruby의 Enumerable 모듈은 반복 가능한 객체에 유용한 메서드를 제공하여 데이터를 쉽게 조작할 수 있게 해줍니다.