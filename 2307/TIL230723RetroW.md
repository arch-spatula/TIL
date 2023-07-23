# TIL

1일1커밋 무사고: 242일차

00:00

## todo

- [ ] 이력서 맞춤법 검사
- [ ] flash card
  - [ ] backend 작업
    - [ ] email 존재여부 get 요청
    - [ ] 계정 삭제 요청
    - [ ] deno deploy docker image 찾기
    - [ ] 배포환경 바꿔보기
  - [ ] frontend
    - [ ] card side useReducer로 리팩토링
- [ ] 원티드 8월 프론트엔드 특강 수강신청
- [ ] 코테
- [ ] 사람인 확인하기
- [ ] ~~아침에 함수형 코딩 50분 2회 이상 독서하기~~
  - [ ] ~~1뽀모도로~~
  - [ ] ~~1뽀모도로~~
- [x] 타입스크립트 데코레이터 만들면서 이해하기
- [x] 블로그 배포
- [x] 주간회고
- [x] 무료 배포 서비스 알아보기

Ben Awad

## 주간회고

- [ ] 아침에 함수형 코딩 50분 2회 이상 독서하기
- [x] 블로그 다시 배포하기
- [ ] flash card backend 작업 진행
  - [ ] email 존재여부 get 요청
  - [ ] 계정 삭제 요청
  - [x] mongoDB fetch 리팩토링
  - [x] super oak로 테스트 코드 작성

별로 이룬것이 없습니다. 수단과 방법을 가리지말고 최대한 많은 것을 달성해야 하는데 안 했습니다. 하루 중 중간중간 목표설정을 잘 못하고 있습니다.

### Liked

- flash card 배포 후 회고를 했습니다.
- 사람인 이력서 지원을 시작했습니다. 지원했다는 사실 자체를 기뻐할 것입니다.
  - 합격이 있으면 문자가 올것이라는 것을 알고 있습니다. 합격을 딱히 기대할 필요는 없을 것 같습니다.

### Learned

- deno를 백엔드로 활용하기에는 현재는 시기상조입니다.
  - 규모가 작은데 조금식 규모를 키우면서 해결한 문제보다 만들어지는 문제가 더 많습니다. 즉 기술 선택을 잘못했습니다.
  - 테스트 코드를 작성하는 예시를 더 확보해야 합니다. API 통신과 연결된 코드는 어떻게 테스트하는지 확인해야 합니다.
- Proxy 서버, DNS 서버에 대한 CS 지식을 배웠습니다.
- mongoDB를 사용할 때 mongoose는 편리하다는 것을 배웠습니다. 많은 추상화를 제공해줍니다.

### Lacked

- mongoDB를 더 잘 쓰기 위해 mongoose로 리팩토링했는데 배포환경에서 사용할 수 없었습니다. 비즈니스적인 임펙트가 약했던 주입니다.
- super oak로 테스트 코드를 일부 리팩토링했는데 그렇게 해도 결국에는 한계가 발생했습니다.
  - 마음이 원하는 것은 장기적으로 nest.js로 포팅하고 배포도 바꾸는 것입니다.
- 하루하루 목표설정하는 능력이 너무 약해졌습니다.
- 프로그래밍 시간을 늘려야 합니다. 회고하고 성장을 확인하는 시간도 중요하지만 이번주 집중을 많이 못한 것 같습니다.

### Longed(잘하기 위해 필요한 것)

- 이력서 PMF 검증에 집중하도록 해야 합니다. 표본을 늘리고 탈락을 검증해야 합니다.
  - 다음주는 수량에 집중하도록 합니다. 그리고 그다음주는 커스터마이징에 집중합니다.

### Action Item

- [ ] 이력서 & 자소서 20곳 이상 지원하기
- [ ] 함수형 코딩 완독
- [ ] flash card
  - [ ] backend 작업 진행
    - [ ] email 존재여부 get 요청
    - [ ] 계정 삭제 요청
  - [ ] frontend
    - [ ] card side useReducer로 리팩토링

## 타입스크립트 데코레이터 만들면서 이해하기

타입스크립트에서 이해를 많이 못한 부분이 있는데 데코레이터입니다.

언제 사용하고 어떻게 사용하는지 이해를 못했습니다. 또 문제를 해결하는 사례를 많이 못봐서 효용을 잘 모르겠습니다.

오늘 효용을 알아 보고 싶습니다. 최대한 바닐라에 가깝게 설치하고 활용해보고자 합니다.

[What you need to know about Decorators](https://www.youtube.com/watch?v=bRAcWk9S-6g)

2019년도에 데코레이터도 많이 사용하지 않았던 것 같습니다. 안티패턴, 코드스멜로 간주하고 있습니다.

TypeGraphQL에서 사용하고 있습니다. 메타정보를 추가하는 기능입니다. 라이브러리에게 정보를 전달합니다.

https://www.typescriptlang.org/docs/handbook/decorators.html

`class declaration`, `method`, `accessor`, `property`, `parameter` 5곳에 적용할 수 있습니다.

[Higher-Order Functions: Better than JavaScript Decorators?](https://www.youtube.com/watch?v=iWkfnbdM25M)

고차함수로 Decorators를 대신할 수 있습니다.

[What are Decorators in Javascript? | Javascript Decorator Functions Tutorial](https://www.youtube.com/watch?v=wYs3rv_KFvk)

데코레이터를 활용하면 DRY 원칙을 준수할 수 있습니다.

[The Magic of TypeScript Decorators](https://www.youtube.com/watch?v=O6A-u_FoEX8)

데코레이터는 함수입니다. 소스코드에 기능을 확장하거나 메타데이터에 주석을 추가하는 기능입니다. 과도한 추상화를 주의해야 합니다.

`class declaration`, `method`, `accessor`, `property`, `parameter` 5곳에 적용할 수 있습니다.

https://www.youtube.com/watch?v=Cos-ctPX5hw

함수정의에 사용할 수 없는 것은 단점입니다.

https://dparkjm.com/typescript-decorators

부분적으로 도움되었습니다.
