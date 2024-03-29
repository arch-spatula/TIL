# 사이트 블로커 크롬 확장자를 만들어보자 7일차

1일1커밋 무사고: 397일차

날씨: 구름많음 / 흐리고 비/눈

## 감사일기

1. 신정에 마음에 드는 라멘가게를 방문했습니다. 오늘도 방문하고 싶습니다.

- [ ] ~~키보드 구매~~
- [ ] Next.js npm으로 설치
- [ ] ~~저녁 강남 라멘~~
- [ ] npm audit으로 환경 분석하기
- [ ] 샌드웜 audit 시도하기
- [x] 주간회고

---

## 보드게임 카페를 다닐까?

## 주간 회고

- [ ] 사이트 차단 크롬브라우져 확장자 만들기
  - [x] 리서치
  - [x] 구현
  - [ ] 정리
- [ ] 안전한 개발환경 블로그 글
  - [ ] 언어와 패키지별 컨테이너 개발환경 설정
  - [ ] npm audit 정리
  - [ ] docker audit 정리(블로그 말고 Doc에 정리하기)
- [ ] 건강관리
  - [ ] 목표 몸무게 88.5kg 이하
  - [ ] 아침 셀러드 3회

### Liked

- 정보확보와 개발자로서 새로운 개발경험이 많은 한주였습니다.
- 크롬 확장자를 설정하고 방해물을 잠시 차단하는 도구를 얻었습니다.
- 다름사람들이 접근하기 어려운 에디터를 사용할 수 있게 되었습니다.
  - 생각보다 설정과정이 재미있었습니다.

### Learned

- cypress, playwright 2개의 E2E 테스팅 라이브러리를 사용하고 경험했습니다.
- github actions 도 다루는 경험을 했습니다. 설정은 실패했지만 대략적인 사용법은 익혔습니다. 
- 퇴근하고 neovim 설정을 해봤습니다. 생각보다 쉽게 적용할 수 있었습니다.

### Lacked

- 라이브러리 리서치를 하고 작업을 빨리 끝내야 하는데 못 끝내고 있었습니다.
  - flaky test 문제를 해결하지 못하고 있었습니다.
  - 불필요한 작업에 하루를 날렸습니다. 작업을 더 진행하기 전에 조금만 더 생각해보면 되는데 생각을 안해서 시간을 많이 낭비했습니다. 작업 자체에 대한 설계가 안 된 것입니다. 완수하면 어덯게 되는지 목표 설정을 잘못했습니다.
  - playwright는 목표를 정보 확보라고 생각하고 작업에 임했습니다. 판단을 잘 내릴 수 있게 라이브러리의 특징을 알아내고 적용한다고 생각했습니다.
- 사람을 더 만나야 한다는 피드백은 아주 강한 수준의 아스퍼거 증후군을 극복하라는 피드백입니다.
- 입으로만 다이어트를 하고 있습니다. 진짜 실천이 없습니다.
- 보안이 잘된 개발환경 설정 블로그 글을 이번주 안에 마무리하는데 실패했습니다.

### Longed(잘하기 위해 필요한 것)

- 문제는 일머리입니다. 일머리에 대한 문제는 센스랑 비슷합니다. 아마 센스를 트렌디하게 말하는 것과 비슷해보입니다.
  - 스스로 엔지니어라고 착각하고 살고 있어서 원칙, 방법론이 더 와닿습니다.
    - 목표를 설정하고 완수하면 달성하는 효과를 생각합니다.
    - 달성하기 위한 일렬의 계획을 세웁니다.
    - 작업을 하면서 피드백을 확보할 중간 지점들을 설정합니다. 
    - 피드백을 받고 작업을 조정합니다.
    - 목표가 바뀌고 계획이 바뀌면 마감에 대해서도 변경합니다.
  - 일머리의 다른 문제는 직무별로 다르다는 것입니다. 공통적인 부분도 있지만 다른 부분도 있습니다.
- 사회생활 스킬을 더 길러야 합니다.
- 집중력이 제일 중요합니다. 설정했던 블로그 글 쓰기 목표를 마무리 지어야 합니다.
- 크롬브라우저 확장자를 만드는 방법을 블로그 소재로 생각하고 있었는데 너무 쉬워서 안 다루는 것이 좋다고 생각이 들었습니다.
- Docker 설정을 경험해봤는데 모든 설정을 소개하는 것은 비효율적인 것 같습니다. 필요성이 생긴 시점에 추가하는 방식으로 대응하겠습니다.
- 웹 프론트엔드 엔지니어로서 크롬 확장자말고 퇴근 후 웹개발 경험이 별로 없습니다. 포트폴리오를 porting할 때가 되었습니다. 오랬동안 유지보수하고 학습할 프로젝트가 필요합니다.
- 회사 수습기간도 끝났습니다. 이력서를 갱신해야 합니다. 더이상 노션에 의존하고 싶지 않습니다. 정상적인 PDF 이력서를 다시 만들고 싶습니다.

### Action Item

- [ ] 안전한 개발환경 블로그 글
  - [ ] npm audit
  - [ ] 샌드웜 audit
  - [ ] Docker 자바스크립트를 위한 설정(이정도는 해줍시다)
- [ ] 이력서 작성

## next.js 설치

```sh
npx create-next-app@latest .
```

```sh
npm audit
# found 0 vulnerabilities
```

충격적이게도 보안문제가 없다고 합니다.

그래서 다른 메이저한 라이브러리를 찾고 다시 적용해봐야 겠습니다.


