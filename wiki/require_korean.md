<!--
Meta Description: # Ruby의 `require` 명령어: 라이브러리와 모듈 불러오기 ## 개요 Ruby에서 `require`는 외부 파일, 라이브러리 및 모듈을 현재의 Ruby 프로그램에 포함시키는 데 사용되는 명령어입니다. 이를 통해 코드의 재사용성과 조직성을 높일 수 있습니다. #...
Meta Keywords: require, ruby, 파일을, 경로를, 있습니다
-->

# Ruby의 `require` 명령어: 라이브러리와 모듈 불러오기

## 개요
Ruby에서 `require`는 외부 파일, 라이브러리 및 모듈을 현재의 Ruby 프로그램에 포함시키는 데 사용되는 명령어입니다. 이를 통해 코드의 재사용성과 조직성을 높일 수 있습니다.

## 문서화
### 목적
`require` 명령어는 Ruby 프로그램에서 다른 파일의 코드를 사용할 수 있게 해줍니다. 주로 Gem, 내장 라이브러리, 또는 사용자 정의 모듈을 불러오는 데 사용됩니다.

### 사용법
`require`의 기본 사용법은 다음과 같습니다:

```ruby
require '파일이름'
```

여기서 `'파일이름'`은 불러오고자 하는 Ruby 파일의 경로입니다. 확장자 `.rb`는 자동으로 포함되므로 생략할 수 있습니다.

### 세부사항
- `require`는 파일을 한 번만 로드합니다. 동일한 파일을 여러 번 `require`해도 첫 번째 로드 이후에는 무시됩니다.
- 시스템의 `$LOAD_PATH`에 따라 파일을 검색하므로, 상대 경로나 절대 경로를 명시할 수 있습니다.

## 예제
1. 기본 사용 예제:
   ```ruby
   require 'json'
   
   data = '{"name": "홍길동", "age": 30}'
   person = JSON.parse(data)
   puts person["name"]  # 출력: 홍길동
   ```

2. 사용자 정의 모듈 불러오기:
   파일 `my_module.rb`가 다음과 같이 정의되어 있다고 가정합니다.
   ```ruby
   # my_module.rb
   module MyModule
     def self.greet
       "안녕하세요!"
     end
   end
   ```

   이를 불러오는 방법은:
   ```ruby
   require './my_module'
   
   puts MyModule.greet  # 출력: 안녕하세요!
   ```

## 설명
- **공통적인 오류**: 파일 경로를 잘못 지정할 경우 `LoadError`가 발생합니다. 이 경우 경로를 확인하거나 `$LOAD_PATH`에 추가해야 합니다.
- **파일 중복 로드 방지**: `require`는 동일한 파일을 여러 번 로드하지 않으므로, 코드 중복을 피할 수 있습니다.
- **대안**: `require_relative` 명령어는 현재 파일의 경로를 기준으로 상대 경로를 사용하여 파일을 불러올 때 유용합니다.

## 한 줄 요약
Ruby의 `require` 명령어는 외부 파일이나 라이브러리를 현재 프로그램에 포함시키는 데 사용됩니다.