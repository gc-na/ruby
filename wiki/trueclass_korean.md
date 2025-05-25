<!--
Meta Description: # TrueClass: 루비에서 불리언 값을 나타내는 클래스 ## 개요 TrueClass는 루비에서 불리언(true 또는 false) 값 중 true를 나타내는 클래스입니다. 이는 조건문 및 논리 연산에서 중요한 역할을 하며, 루비의 모든 불리언 연산은 TrueClas...
Meta Keywords: true, 루비에서, trueclass는, trueclass의, 불리언
-->

# TrueClass: 루비에서 불리언 값을 나타내는 클래스

## 개요
TrueClass는 루비에서 불리언(true 또는 false) 값 중 true를 나타내는 클래스입니다. 이는 조건문 및 논리 연산에서 중요한 역할을 하며, 루비의 모든 불리언 연산은 TrueClass와 FalseClass를 통해 처리됩니다.

## 문서화
TrueClass는 루비에서 기본적으로 제공되는 클래스 중 하나로, 불리언 논리의 '참' 값을 나타냅니다. TrueClass의 인스턴스는 주로 조건문에서 사용되며, 주어진 조건이 참인지 여부를 결정하는 데 활용됩니다.

### 목적
TrueClass의 주요 목적은 루비 프로그래밍에서 참(true) 값을 효과적으로 표현하고, 관련된 모든 메서드를 제공하는 것입니다.

### 사용법
TrueClass의 인스턴스는 일반적으로 다음과 같이 사용됩니다:
- 조건문 (if, unless 등)
- 반복문 (each, while 등)

### 세부 사항
- TrueClass는 루비의 내장 클래스이며, 모든 true 값은 이 클래스의 인스턴스입니다.
- false와 nil은 루비에서 "거짓"으로 평가되며, 이외의 모든 값은 "참"으로 평가됩니다.
- TrueClass는 다양한 메서드를 지원하며, 이들 중 일부는 다음과 같습니다:
  - `to_s`: TrueClass 인스턴스를 문자열로 변환합니다.
  - `to_i`: TrueClass 인스턴스를 정수로 변환하며, 1을 반환합니다.
  - `!`: TrueClass의 반대로 false를 반환합니다.

## 예제
```ruby
# TrueClass의 기본 사용 예
if true
  puts "이 조건은 참입니다."
end

# TrueClass 메서드 사용 예
puts true.to_s  # 출력: "true"
puts true.to_i  # 출력: 1
puts !true      # 출력: false
```

## 설명
TrueClass는 루비에서 불리언 로직을 구현하는 데 있어 매우 중요한 요소입니다. 그러나 주의해야 할 점은 루비에서는 false와 nil만이 "거짓"으로 평가된다는 것입니다. 따라서 개발자는 조건문을 작성할 때 이러한 특성을 이해하고 있어야 합니다. 또한, TrueClass의 메서드를 잘 활용하면 코드의 가독성을 높일 수 있습니다.

## 한 줄 요약
TrueClass는 루비에서 참(true) 값을 나타내는 클래스이며, 조건문 및 논리 연산에서 필수적인 역할을 수행합니다.