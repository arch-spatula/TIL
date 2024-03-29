# TIL

1일1커밋 무사고: 203일차

04:59

## todo

- [ ] 이메일, 비밀번호 유효성 검사
- [ ] 회원가입 페이지 구현
- [ ] 카드 컴포넌트 구현
- [ ] 복습 주기별 카드 컴포넌트 묶어 놓은 덱 페이지 구현
- [ ] 리액트 프로파일링으로 문제 분석해보기
- [ ] 리액트 쿼리로 통신
- [ ] 리액트 쿼리로 optimistic update 패턴 구현
- [ ] 리액트 쿼리로 무한 스크롤 구현
- [ ] API Mocking
- [ ] 회원가입 피드백
- [ ] 카드 만들기(덱 페이지에서 추가)
- [ ] 토큰 갱신 인터셉터 구현(refresh token session storage에서 갱신처리하기)
- [ ] 추가 기능 구현
  - [ ] 검색 구현
  - [ ] nav 테스트 코드 작성
  - [ ] 로그인 페이지 happy-path 테스트 코드
  - [ ] helperText state machine 패턴
  - [ ] useInput에 input focus 기능 추가
  - [ ] page 컴포넌트 mock하는 방법 찾기
  - [ ] suspense 고도화
  - [ ] 로그인 페이지 화면과 비즈니스 로직 분리
  - [ ] container-query 적용
  - [ ] next.js로 리팩토링
- [ ] 그냥 해보고 싶은 작업
  - [ ] 6주차 리액트 cookbook 배포
  - [ ] Docker Volume 설정하기
- [x] 주간회고

## 예비군 가는 길 확인하기

## 르블랑의 법칙 vs YAGNI 원칙

오버엔지니어링과 언더 엔지니어링 사이 딜레마입니다.

## 주간회고

- 월간 목표
  - [ ] 프론트엔드 프로덕트 MVP 릴리즈
  - [ ] 이력서 리팩토링
    - [ ] 이력서 심미성은 보류하고 순수하게 내용위주로 변경
    - [ ] 비즈니스적으로 문제로 인식한 것부터 역할과 성과 그리고 의사결정 과정 정리(문제-행동-결과)
  - [ ] 포트폴리오 페이지 만들기
    - [ ] 상세 달성 성과 나열하기
  - [ ] 코테와 면접 질문은 꾸준히 진행하기
    - 면접 질문은 복습 시스템 만들기 시작하기
    - 코테는 기출 문제 위주로 점진적으로 옮기기
    - 자료구조 알고리즘은 다른 복습 자료 활용하고 추가하기
- 주간 목표
  - [x] token testing
  - [ ] Deno oak 테스트 코드 작성
    - [ ] user
    - [ ] cards
  - [x] API 명세 구체화(에러 응답 요인들)
  - [x] route 컴포넌트 리팩토링
  - [x] 1.1 API 수정
  - [x] 로그인 페이지 구현
  - [x] 회원가입 페이지 구현
  - [x] 로그아웃 기능 구현
  - [ ] 로그아웃 미들웨어 구현
  - [ ] 토큰 갱신 인터셉터 구현
  - [ ] 카드 컴포넌트 구현
  - [ ] 복습 주기별 카드 컴포넌트 묶어 놓은 덱 페이지 구현
  - [x] 모노톤 위주로 간단한 스타일링(tailwind 컬러 활용)
  - [x] font 고르고 설정하기
  - [ ] 리액트 프로파일링으로 문제 분석해보기
  - [x] 리액트 스피너 설치
  - [x] 카드 모델 클래스 구현
  - [ ] API Mocking
  - [ ] 리액트 쿼리로 통신
  - [ ] 리액트 쿼리로 optimistic update 패턴 구현
  - [ ] 리액트 쿼리로 무한 스크롤 구현
  - [ ] 그냥 해보고 싶은 작업
    - [ ] 6주차 리액트 cookbook 배포
    - [ ] Docker Volume 설정하기

### Liked

- 고통받은 만큼 성장한다고 하면 token으로 고통을 많이 받아서 많이 성장했습니다.
- 하루에 한 작업을 기록하니까 생각보다 많은 것을 학습했다는 것을 확인할 수 있었습니다.

### Learned

- cookie는 도메인이 같아야 한다는 문제를 고통스러운 방식으로 배웠습니다.
- token의 기간별 처리 정책도 배웠습니다.
- Deno런타임에서 테스트 코드를 작성하는 방법을 배웠습니다.
- RRD의 Data router를 훔쳐배웠습니다.
- 도메인 객체의 존재를 알게 되었습니다. 아직 적용을 완전히 못했습니다.
- vite 플러그인을 설치하고 활용하는 법을 알게 되었습니다.
- 프론트엔드 테스트 전략 패러다임을 알게 되었습니다. 하지만 실천은 못하고 있습니다. 정적 분석과 결합테스트에 집중해야 한다는 것만 알고 있지만 적용을 위해 다른 병목지점들이 있습니다.
- 테스트코드를 작성하는 패턴을 알게 되었습니다. BDD, Given-When-Then 패턴의 존재를 알게 되었습니다.
- https는 서버에만 적용되어 있으면 괜찮다는 것도 배웠습니다. 클라이언트는 개발환경인 localhost의 http 프로토콜이어도 괜찮습니다. 이것도 고통스러운 방식으로 학습했습니다. 물론 vite 플러그인에 대해서 알 수 있게 되었습니다.
- RRD에도 Provider 설정 방법도 배웠습니다.
- Jotai에서 localStorage를 활용하는 방법을 배웠습니다. 작고 편리한 라이브러리입니다.
- Container Query는 현재 CSS만 적용되어 있다는 것을 배웠습니다. 다른 라이브러리 설치가 현재 필요하다는 것을 알게 되었습니다. module css가 그렇게 나쁘지 않다는 것 관점이 생겼습니다.
- lazy loading을 위해서 code splitting을 하려면 `default export`로 처리해야 한다는 것을 학습했습니다. 하지만 왜 `default export`로 처리해야 하는지는 모릅니다. virtual-DOM에서 어떻게 처리하는지 감도 안 잡힙니다.
  - 약간의 검색을 해보면 번들링의 동작방식의 문제라고 합니다. 번들링을 할 때 모듈별 고유 식별자를 구분하는 기준이 `default export`이라는 점입니다.
  - default export가 일반적으로 best practice라는 점을 code splitting을 통해서 학습할 수 있게 되었습니다.

### Lacked

- 지난주 설정 지옥을 지나서 이번주는 token과 auth 지옥으로 건너왔습니다. 그만큼 기초가 너무 없었다는 것입니다.
- 의욕이 너무 없었습니다. 하루 12시간 정도 집중하면서 작업하고 만들어야 합니다.
- auth, token은 기본인데 너무 많은 시간을 들였습니다. 기초가 없어서 프로젝트가 늘어졌습니다.
- 프로젝트를 시작하면서 기술 스택을 잘 못 선택해서 기술부채가 많이 늘었습니다. 테크 트렌드는 취미고 본업은 최대한 보수적으로 접근해야 합니다. 활용할 표면적인 리소스가 많다고 능사는 아닙니다.
- 프로젝트를 빨리 끝내야 하는데 학습에 더 집중하고 있습니다. 학습보다 더 중요한 것은 취업입니다.

### Longed(잘하기 위해 필요한 것)

- 언젠가는 session 기반 서버도 만들어봐야 합니다. 기초가 없다는 몇가지 구성 요소를 검증하는데 성공했습니다.
- 관심사를 잘 분리하는 코드를 아직도 모릅니다. 양산형 국비지원 교육의 한계입니다. 코드 퀄리티는 기본 중 기본인데 가르치지 않았습니다.
  - 관심사를 아주 잘 나누는 능력을 보여줄 수 있어야 합니다. 아직도 화면과 비즈니스로직이 결합되어 있습니다. 비즈니스 로직은 독립적이어야 합니다. 화면은 화면대로 독립적으로 동작해야 합니다.
- 테스트 코드를 공부하면서 시간낭비를 너무 많이하고 있습니다. 테스트는 기본 맞고 유지보수를 위해서 필요한 기본 중 기본입니다. 이 기본이 없어서 이 프로젝트로 학습하는데 시간낭비를 너무 많이하고 있습니다. 지금 시점에서 테스트는 마이너하고 기능추가가 메이저하면 테스트코드 작성을 뒤로 할 수 있어야 합니다.
- 다음주는 시간이 정말 없습니다. 그 다음주까지 계획해야 합니다.
- 프로젝트를 빨리 끝내야 합니다. 테스트 코드를 보류해도 빨리 끝내야 합니다. 그리고 테스트 코드를 추가하고 리팩토링하기 좋은 환경을 만드는 능력을 보여줄 수 있어야 합니다.
- 비즈니스 문제를 찾아야 합니다. 그리고 비즈니스 문제를 기술적으로 해결한 사례를 추가해야 합니다. 문제는 아주 작은 앱에 비즈니스 문제를 찾고 정의를 어떻게 해야 할지 모르겠습니다.
  - 면접관 입장에서 주된 관심사는 기술을 활용해서 비즈니스 문제를 풀어내는 사람이라는 가설을 갖고 있습니다. 이 가설을 검증하기 위해서 비즈니스 문제를 찾아야 합니다. 그리고 해결하고 이력서에 추가해야 합니다.
- 예비군을 잘 다녀와야 합니다.

### Action Item

- [ ] 4일 출퇴근 예비군 잘 다녀오기
- [ ] ???

## Million.js

High-school student makes React a million times faster

https://www.youtube.com/watch?v=VkezQMb1DHw

fireship이 소개한 새로운 리액트 프레임워크입니다. 생각보다 기능이 작습니다. 그래서 더 좋습니다.

하지만 중요한지 판단하기 어렵습니다. 좋은 성능을 쉽게 뽑는다는 점은 좋지만 리액트가 아닌 프레임워크와 라이브러리를 활용해보고 싶습니다.
