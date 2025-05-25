<!--
Meta Description: # Ruby의 "or" 연산자: 사용법과 예제 ## 개요 Ruby 프로그래밍 언어에서 "or"는 논리 연산자로, 두 개의 조건 중 하나라도 참일 경우 참을 반환합니다. 이 연산자는 조건문을 작성할 때 매우 유용하게 사용됩니다. ## 문서화 "or" 연산자는 Ruby에서...
Meta Keywords: result, condition1, ruby, 연산자는, condition2
-->

# Ruby의 "or" 연산자: 사용법과 예제

## 개요
Ruby 프로그래밍 언어에서 "or"는 논리 연산자로, 두 개의 조건 중 하나라도 참일 경우 참을 반환합니다. 이 연산자는 조건문을 작성할 때 매우 유용하게 사용됩니다.

## 문서화
"or" 연산자는 Ruby에서 논리 연산을 수행하는 방법 중 하나입니다. 두 개의 표현식이 주어졌을 때, "or" 연산자는 첫 번째 표현식이 참이면 그 값을 반환하고, 그렇지 않으면 두 번째 표현식의 값을 반환합니다. 주의할 점은 "or"의 우선순위가 "and"보다 낮기 때문에, 복잡한 조건문에서는 괄호를 사용하는 것이 좋습니다.

### 사용법
```ruby
result = condition1 or condition2
```

이 구문에서 `condition1`이 참이면 `result`는 `condition1`의 값을 가지며, 그렇지 않으면 `condition2`의 값을 갖습니다.

## 예제
```ruby
# 예제 1: 기본 사용법
x = nil
y = "Hello"
result = x or y
puts result  # 출력: "Hello"

# 예제 2: 조건문에서의 사용
is_logged_in = false
is_admin = false

access = is_logged_in or is_admin
puts access  # 출력: false
```

## 설명
"or" 연산자는 조건문에서 직관적으로 읽힐 수 있도록 도와줍니다. 그러나 "or"의 우선순위가 낮기 때문에, 다음과 같은 경우 혼동을 초래할 수 있습니다:

```ruby
result = condition1 or condition2
```
위 코드는 `result`에 `condition1`의 값이 할당된 후 `condition2`를 평가합니다. 즉, `result`는 항상 `condition1`의 값이 됩니다. 이를 방지하기 위해 괄호를 사용하여 명확히 할 수 있습니다:

```ruby
result = (condition1 or condition2)
```

또한, `||` 연산자와의 차이점도 주의해야 합니다. `||`는 더 높은 우선순위를 가지며, 짧은 회로 평가(short-circuit evaluation)를 수행합니다. 즉, 첫 번째 조건이 참일 경우 두 번째 조건을 평가하지 않습니다.

## 한 줄 요약
Ruby에서 "or" 연산자는 두 조건 중 하나라도 참일 경우 참을 반환하는 논리 연산자입니다.