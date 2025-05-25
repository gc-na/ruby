<!--
Meta Description: # Ruby의 ensure: 오류 처리 및 자원 정리 ## 개요 Ruby의 `ensure` 키워드는 예외 처리 블록에서 사용되며, 프로그램 실행 중 오류가 발생하더라도 항상 실행되는 코드를 정의하는 데 사용됩니다. 이는 자원을 정리하거나 특정 작업을 완료해야 할 때 유...
Meta Keywords: ensure, puts, file, ruby의, rescue
-->

# Ruby의 ensure: 오류 처리 및 자원 정리

## 개요
Ruby의 `ensure` 키워드는 예외 처리 블록에서 사용되며, 프로그램 실행 중 오류가 발생하더라도 항상 실행되는 코드를 정의하는 데 사용됩니다. 이는 자원을 정리하거나 특정 작업을 완료해야 할 때 유용합니다.

## 문서화
`ensure`는 Ruby의 예외 처리 구조인 `begin-rescue` 블록과 함께 사용됩니다. `ensure` 블록 내의 코드는 예외가 발생하더라도 항상 실행되며, 예외가 발생하지 않더라도 실행됩니다.

### 목적
- 자원 정리: 파일 닫기, 데이터베이스 연결 해제와 같은 작업 수행.
- 예외 발생 여부에 관계없이 특정 코드 실행 보장.

### 사용법
다음은 `ensure`를 사용하는 기본적인 구조입니다:

```ruby
begin
  # 위험한 코드
rescue SomeError => e
  # 예외 처리
ensure
  # 항상 실행되는 코드
end
```

## 예제
### 기본 사용 예
```ruby
def divide(a, b)
  begin
    result = a / b
  rescue ZeroDivisionError
    puts "0으로 나눌 수 없습니다!"
    return nil
  ensure
    puts "연산이 완료되었습니다."
  end
  result
end

puts divide(10, 2) # => 5
puts divide(10, 0) # => 0으로 나눌 수 없습니다!
                     # 연산이 완료되었습니다.
```

### 파일 작업에서의 사용 예
```ruby
def read_file(file_path)
  file = File.open(file_path)
  # 파일에서 데이터 읽기
  data = file.read
rescue Errno::ENOENT
  puts "파일을 찾을 수 없습니다!"
ensure
  file.close if file # 파일이 열려 있을 경우 닫기
end
```

## 설명
- **공통적인 함정**: `ensure` 블록 내에서 발생하는 예외는 무시됩니다. 즉, `ensure` 블록에서 예외가 발생하면, 해당 예외는 프로그램을 종료시키거나 더 이상 진행되지 않을 수 있습니다. 따라서 `ensure` 블록에서는 안전한 코드를 작성하는 것이 중요합니다.
- **전역 상태**: `ensure` 블록은 메서드의 반환값에 영향을 미치지 않지만, 메서드 내에서 정의된 변수를 접근할 수 있습니다. 이는 예외 발생 여부와 관계없이 실행된다는 점에서 유의해야 합니다.

## 한줄 요약
Ruby의 `ensure` 키워드는 예외 처리 블록 내에서 오류 발생 여부와 관계없이 항상 실행되는 코드를 정의하는 데 사용됩니다.