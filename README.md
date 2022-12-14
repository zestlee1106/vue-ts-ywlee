# Vue Todo with Typescript

- Vue2 + Typescript 프로젝트
- vue cli 로 Typescript 베이스 프로젝트를 만듦
- .vue 파일 생성할 때 Vetur extension 으로 도움을 받을 수 있음 (템플릿 자동완성 등)
- .vue 파일에서의 타입 스크립트 정의 방식을 확인함
  - data
    - 초기화를 할 때 as 로 타입을 정해 줄 수 있음
    - 타입을 정해 주면, 해당 변수에 다른 타입의 값이 들어왔을 때 에러를 발생시켜 줌
    - 의도하지 않은 동작을 방지할 수 있음 (secure coding)
  - methods
    - 반환 타입을 정의할 수 있음
    - 파라미터의 타입을 정의할 수 있음
      - 파라미터에 원하지 않는 타입이 들어가는 경우를 방지할 수 있음
  - props
    - 기본적으로 Validation 으로 해 줬으나, as 로 타입을 정하여 더욱 안전한 ts 를 작성할 수 있음
    - as 로 타입을 정해주고 싶을 땐, PropType 을 사용해야 함 (PropType\<Todo>)
  - computed
    - 반환 타입을 정해 줘야 다른 것들도 올바른 추론을 받을 수 있음

## 그렇다면 타입스크립트의 이점은 무엇일까

1. 의도치 않은 에러를 방지할 수 있다. <br/>
   _타입을 미리 지정해놓음으로써 런타임 에러를 줄일 수 있음_
2. IDE 의 자동완성 기능의 도움을 받을 수 있다. <br/>
   _interface로 선언을 해 놓을 경우, 해당 객체로 접근했을 때 자동완성이 됨_

--> 현재 드는 생각은, API 통신을 할 때 가장 빛을 볼 수 있을 것 같다. <br/>
--> 왜냐하면, 응답 데이터의 구조를 미리 interface 로 잡은 다음, 해당 API 를 호출할 때의 로직에서 런타임 에러를 줄일 수 있다는 생각이 들기 때문!
