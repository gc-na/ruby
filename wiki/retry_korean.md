<!--
Meta Description: # Ruby에서의 "retry": 오류 처리의 핵심 ## 개요 Ruby의 `retry` 키워드는 예외 처리에서 사용되며, 특정 코드 블록이 실패했을 때 이를 다시 시도하도록 할 수 있습니다. 주로 `begin-rescue` 구문과 함께 사용되어, 오류가 발생했을 때 유...
Meta Keywords: retry, begin, rescue, 예외가, attempts
-->

# Ruby에서의 "retry": 오류 처리의 핵심

## 개요
Ruby의 `retry` 키워드는 예외 처리에서 사용되며, 특정 코드 블록이 실패했을 때 이를 다시 시도하도록 할 수 있습니다. 주로 `begin-rescue` 구문과 함께 사용되어, 오류가 발생했을 때 유용하게 활용됩니다.

## 문서화
`retry`는 Ruby의 예외 처리 메커니즘에서 중요한 역할을 합니다. 이 키워드는 예외가 발생한 후, 이전 코드 블록을 다시 실행하도록 지시합니다. `retry`는 일반적으로 `begin` 블록 내에서 사용되며, 예외가 발생했을 때 `rescue` 블록으로 제어가 넘어갑니다. 이후 `retry`가 호출되면, 프로그램은 `begin` 블록의 처음으로 돌아가서 코드를 다시 실행합니다.

### 사용법
```ruby
begin
  # 실행할 코드
rescue SomeException => e
  # 예외 처리 코드
  retry # 예외가 발생했을 때 코드를 다시 시도
end
```

## 예제
다음은 `retry`를 활용한 기본적인 예제입니다:

```ruby
def unreliable_method
  # 임의로 실패하는 코드
  raise 'Something went wrong!' if rand > 0.5
  puts 'Success!'
end

attempts = 0

begin
  attempts += 1
  unreliable_method
rescue => e
  puts "Error occurred: #{e.message}. Attempt ##{attempts}."
  retry if attempts < 3 # 최대 3번 시도
end
```

이 예제에서는 `unreliable_method`가 실패할 경우, 최대 3번까지 다시 시도합니다.

## 설명
`retry`를 사용할 때 주의해야 할 점은 무한 루프에 빠지지 않도록 하는 것입니다. 예외가 지속적으로 발생하는 경우, `retry`는 이전 코드 블록을 계속 재시도하여 프로그램이 멈추지 않게 됩니다. 따라서, 최대 재시도 횟수를 설정하거나 적절한 종료 조건을 두는 것이 필수적입니다. 

또한, `retry`는 `begin` 블록의 처음으로 돌아가기 때문에, 이전 상태를 유지하지 않습니다. 즉, `begin` 블록 내에서 선언된 변수들은 매번 새롭게 초기화됩니다. 그러므로 상태를 유지해야 하는 경우에는 다른 방법을 고려해야 합니다.

## 한 줄 요약
Ruby에서의 `retry`는 예외 발생 시 이전 코드를 다시 시도하도록 하는 유용한 키워드입니다.