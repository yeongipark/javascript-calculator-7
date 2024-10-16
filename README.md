### 구현할 기능 목록 정리

1. 상수 저장하기

   - 1.1 에러 메시지 상수 저장

   - 1.2 입출력 메시지 상수 저장

2. 시작 문자열 출력하기

3. 사용자에게 문자열 입력받기

4. 입력값 유효성 검사하기

   - 4.1 숫자로 시작하는 경우

     - 4.1.1 `,` `:` 외 다른 문자 포함시 예외 처리

     - 4.1.2 `,` `:` 두 구분자가 동시에 나오는 경우 예외 처리

   - 4.2 `//`로 시작하는 경우

     - 4.2.1 `\n`존재하지 않으면 예외 처리

     - 4.2.2 `\n`까지의 문자가 빈 문자열인 경우 예외 처리

     - 4.2.3 `\n`까지의 문자와 `,` `:` 외 다른 문자 포함시 예외 처리

     - 4.2.4 구분자가 동시에 나오는 경우 예외 처리

   - 4.3 이외의 경우는 예외 처리

5. 입력값 구분자로 분리후 더하기 연산 수행

6. 결과 출력하기

### 예외 목록

- 숫자로 시작하는 경우

  - `-1,2:3` => `[ERROR] 양수만 입력해 주세요`

  - `1,2a3` => `[ERROR] 구분자로 쉼표와 클론만 사용해 주세요`

- "//"로 시작하는 경우

  - `//1,2,3` => `[ERROR] \n을 포함시켜 주세요`

  - `//\n1,2,3` => `[ERROR] 커스텀 구분자를 입력해 주세요`

  - `//abc\n1,2abc3d4` => `[ERROR] 커스텀 구분자 혹은 쉼표와 클론만 사용해 주세요`

- 그외 경우
  - `a1b22` => `[ERROR] 입력값을 확인해 주세요 `
