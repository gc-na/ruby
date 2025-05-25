<!--
Meta Description: # Ruby의 rescue: 예외 처리를 위한 필수 키워드 ## 개요 Ruby에서 `rescue`는 예외 처리 메커니즘의 핵심 요소로, 프로그램 실행 중 발생할 수 있는 오류를 우아하게 처리하는 데 사용됩니다. 이를 통해 코드의 안정성을 높이고 예외 상황에 대한 대처를...
Meta Keywords: rescue, 예외를, begin, puts, 발생할
-->

# Ruby의 rescue: 예외 처리를 위한 필수 키워드

## 개요
Ruby에서 `rescue`는 예외 처리 메커니즘의 핵심 요소로, 프로그램 실행 중 발생할 수 있는 오류를 우아하게 처리하는 데 사용됩니다. 이를 통해 코드의 안정성을 높이고 예외 상황에 대한 대처를 용이하게 합니다.

## 문서화
`rescue`는 `begin` 블록 내에서 발생하는 예외를 포착하여 처리할 수 있게 합니다. Ruby에서는 예외가 발생하면 실행 흐름이 중단되며, `rescue`를 사용하면 이러한 예외를 처리하고 프로그램이 비정상 종료되는 것을 방지할 수 있습니다.

### 용도
- 예외를 포착하고 처리하여 프로그램의 안정성을 높임
- 사용자에게 친숙한 오류 메시지를 제공
- 프로그램의 특정 부분에서 발생할 수 있는 예외를 관리

### 사용법
`rescue`는 `begin` 블록과 함께 사용됩니다. 기본적인 구조는 다음과 같습니다:

```ruby
begin
  # 예외가 발생할 수 있는 코드
rescue StandardError => e
  # 예외 처리 코드
  puts "오류 발생: #{e.message}"
end
```

## 예제
### 기본 사용 예
다음은 `rescue`를 사용하여 나누기 연산에서 발생할 수 있는 예외를 처리하는 간단한 예제입니다.

```ruby
def divide(a, b)
  begin
    result = a / b
    puts "결과: #{result}"
  rescue ZeroDivisionError => e
    puts "오류 발생: 0으로 나눌 수 없습니다! #{e.message}"
  end
end

divide(10, 2)  # 결과: 5
divide(10, 0)  # 오류 발생: 0으로 나눌 수 없습니다!
```

### 여러 예외 처리
여러 개의 예외를 처리할 수도 있습니다:

```ruby
begin
  # 코드 블록
rescue ZeroDivisionError
  puts "0으로 나누는 오류!"
rescue ArgumentError
  puts "잘못된 인자 오류!"
end
```

## 설명
`rescue`를 사용할 때 주의해야 할 몇 가지 사항이 있습니다:

- **구조**: `begin` 없이 `rescue`를 사용할 수 없으며, 항상 `begin` 블록과 함께 사용해야 합니다.
- **예외 클래스**: 특정 예외를 처리할 수 있지만, 모든 예외를 처리하는 경우에는 `StandardError`를 명시해야 합니다. 모든 예외를 포괄적으로 처리하려면 `rescue` 뒤에 아무것도 적지 않으면 됩니다.
- **중첩 처리**: `begin-rescue` 블록을 중첩하여 사용할 수 있으나, 지나치게 복잡한 구조는 피하는 것이 좋습니다.

## 한 줄 요약
Ruby에서 `rescue`는 예외를 처리하여 프로그램의 안정성을 높이는 중요한 키워드입니다.