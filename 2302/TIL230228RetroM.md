1일1커밋 무사고: 106일차

# 감사일기

1. `// ^?`에 감사합니다. 마우스에 의존하지 않고 타입을 확인할 수 있었습니다.
2. 타입스크립트 핸드북에 감사합니다. `instanceof`를 발견하고 적용할 수 있었습니다.
3. 오늘 프로그래밍이 재미있어서 감사합니다. 내일도 취미를 위한 프로그래밍을 또해볼 것입니다.

01:29

# todo

- [x] 배너 이미지

# 영단어

- 모든 영어 모음: A, E, I, O, U
- 개발 설정: configuration, configure
- 프리티어: prettier
- 컨트롤러: controller
- 감싸는 태그: Wrapper
- 사이: between
- 팩토리 패턴: factor pattern
- CPU: Central Processing Unit
- 리텐션: retention
- 메모리: memory
- 클로저: closer

# 월간 회고

- [ ] 클래스형 컴포넌트를 통해 라이프사이클 hook을 정확이 다를 수 있도록 합니다.
- [x] Next.js를 다루기 시작합니다.
- [ ] express.js로 todo app이라도 만듭니다.
  - [ ] Next.js를 더 깊있게 이해하기 위해서 간단하게라도 학습합니다.
- [ ] 웹 소캣, 웹 TRC를 다루기 시작합니다.
- [ ] CS 깊은 지식으로 진입하기 시작합니다.
  - [ ] 컴퓨터 역사를 정리하기 시작합니다.
  - [ ] 하드웨어 컴퓨터 구조를 배웁니다.
  - [ ] 운영체제를 다루기 시작합니다.
  - [ ] 네트워크 통신을 다룹니다.
  - [ ] 프론트엔드에 집중하는 보안을 다룹니다.
  - [ ] 데이터 베이스 이론을 배우기 시작합니다.
- [ ] 자료구조와 알고리즘 개념이 있어야 풀 수 있는 문제를 풀기 시작합니다.
- [ ] git과 github에서 자주 발생하지만 더 어려운 유스케이스를 대응해야 합니다.

- [ ] [Zod](https://www.totaltypescript.com/tutorials/zod)
- [ ] [Confidently Testing Redux Applications with Jest & TypeScript](https://egghead.io/courses/confidently-testing-redux-applications-with-jest-typescript-16e17d9b)
- [ ] [RTK Query Basics: Query Endpoints, Data Flow and TypeScript](https://egghead.io/courses/rtk-query-basics-query-endpoints-data-flow-and-typescript-57ea3c43)
- [ ] [mostly-adequate-guide](https://github.com/MostlyAdequate/mostly-adequate-guide)

설정했던 목표입니다. 달성한 것이 하나도 없습니다.

Zod는 스키마 검증으로 활용하기 애매했습니다. 대형 어플리케이션을 만드는 상황이 아닌 이상 필요성이 부차적이었던 것 같습니다. redux testing은 도입이 어려웠던 이유는 코드 베이스가 과거였고 현재 버전으로 리팩토링하기가 어려웠습니다. RTK Query는 따로 공부하게되었습니다. redux를 타입스크립트로 설정도 해봤습니다. 함수형 프로그래밍 도서는 함수형 프로그래밍이 필요할 정도로 로직의 규모가 거대하지는 않았습니다. 요즘에는 필요성을 느끼기 시작했습니다.

Next.js는 이루었습니다. 클래스형 컴포넌트는 과정이 끝나고 튜토리얼을 보고 빠르게 정리할 수 있습니다. CS 깊은 지식을 위한 노력은 수료직후부터 시작인 것 같습니다. 결국 면접 준비하면서 공부해야 할 내용들이었습니다. 자료구조와 알고리즘은 짬내는 것이 어려웠기 때문에 실천이 어려웠습니다. git과 github 복잡한 유스케이스는 필요성 문제 였습니다. 지금은 리베이스가 필요없다고 느껴지지만 정상적인 회사에서는 리베이스를 자주 하게 될 것이라고 예상할 수 있습니다.

## Liked

- 계속 알려줘야 하는 사람에서 그렇게 하지 않아도 되는 사람이 되었습니다.

## Learned

- 데이터 베이스 선택은 굉장히 보수적으로 접근할 필요가 있습니다. react-query랑 같이 사용하기 위해 supabase를 사용하는 것 자체는 좋습니다. 쿼리 캐시 조작 문제를 커버할 수 있습니다.

## Lacked

- supabase 지식이 많이 없었습니다. RLS 설정을 팀원이 하게 했습니다. 필요하면 SQL문을 작성했어야 했는데 지식이 없었습니다. 데이터베이스 선택에 너무 많은 리스크 테이킹을 했습니다.
- 많은 부분에서 성장이 없었습니다. 자바스크립트 코어를 배울 때랑 다릅니다. 또 리액트를 배울 때랑도 다릅니다. 많은 것을 흡수했다는 달이 아니었습니다.
- 모르는 것에 대해서 파악을 못하고 있었습니다.
  - 실무적으로 Set, Map은 분명히 활용될 자료형입니다.
  - Symbol도 정리하고 활용법을 배워야 합니다.
  - 제너레이터와 이터레이터가 무엇이고 어떻게 사용하는지 모릅니다.
  - 자바스크립트의 정규표현식을 모릅니다.
- 쓸때 없는 걱정이 많습니다. 잔불안이 너무 많습니다.
- 지난달 결심 대부분을 못 이루었습니다. 중간에 무엇을 기각할 때는 무슨 맥락에서 가치가 사라진 것이 기록이 필요합니다. 하지만 그 부분이 없었습니다.
- 팀프로젝트 이외에 개인 프로젝트 1개를 만들고 싶습니다.

## Longed(원하는 것)

- SQL문 작성을 배워서 기초 중 하나를 보충합니다.
- 생활코딩 튜토리얼로 자바스크립트 정규표현식을 이해하고 싶습니다. 대략적인 패턴부터 이해하고 싶습니다.
- 시간이 걸릴 로우레벨 기초 CS 지식을 얻고 싶습니다. IT 시장이 불황이기 때문에 준비 기간을 길게 준비하는 것은 선택사항이 아닌 것 같습니다.

## Action Item

- C언어를 통해 메모리관리를 안 하는 언어로 기초 CS 지식쌓기
  - [ ] [C Programming Tutorial for Beginners](https://www.youtube.com/watch?v=KJgsSFOSQv0) 튜토리얼 정리하기
  - [ ] [<독하게 시작하는 C 프로그래밍>](http://www.yes24.com/Product/Goods/18732021) 읽기
  - [ ] [Harvard CS50 – Full Computer Science University Course](https://www.youtube.com/watch?v=8mAITcNt710) 강의 수강
  - [ ] 네이버 지식백과 전선학 개론 1회독
    - [ ] 컴퓨터 역사를 정리하기 시작합니다.
    - [ ] 하드웨어 컴퓨터 구조를 배웁니다.
    - [ ] 운영체제를 다루기 시작합니다.
    - [ ] 네트워크 통신을 다룹니다.
    - [ ] 프론트엔드에 집중하는 보안을 다룹니다.
    - [ ] 데이터 베이스 이론을 배우기 시작합니다.
- 자료구조와 알고리즘
  - [ ] 자바스크립트 자료구조 알고리즘 유데미 완강
  - [ ] [JavaScript Algorithms and Data Structures - Codevolution](https://www.youtube.com/watch?v=coqQwbDezUA&list=PLC3y8-rFHvwjPxNAKvZpdnsr41E0fCMMP)
  - 생활코딩 자바스크립트 정규표현식
- SQL 지식 습득
  - [ ] [SQL Tutorial - Full Database Course for Beginners](https://www.youtube.com/watch?v=HXV3zeQKqGY)
- 정규표현식 정리
