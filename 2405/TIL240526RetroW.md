# 독하게 시작하는 C 읽기 57일차

1일1커밋 무사고: 531일차

## 감사일기

1. ???

- [x] 주간회고
- [x] 주간줍줍
- [ ] 블랙잭 만들기
  - [ ] 게임 루프
    - [ ] 덱 드로우 카운터
    - [ ] 카드 2장 오픈
    - [ ] 승부 판정
    - [ ] 배당
  - [ ] 덱 구현
    - [ ] 덱 사이즈 조절 로직
- [ ] 플래시 카드 2.0 서비스 만들기
  - [ ] nuxt 설치
  - [ ] mongoose ORM 설치
  - [ ] vercel 배포
  - [ ] 로그인 구현
  - [ ] 어드민 전용기능(배치 삭제, 생성 제한)
  - [ ] 핀터레스트 레이아웃 구현
  - [ ] 문제 유형 태그 구현
  - [ ] 카나리 설정
- [ ] 정보처리 기사 문제집 기본서 시작하기
  - [ ] 소프트웨어 1 ~ 5장
    - [ ] 1장 소프트웨어 설계
    - [ ] 2장 소프트웨어 개발
    - [ ] 3장 데이터베이스 구축
    - [ ] 4장 프로그래밍 언어 활용
    - [ ] 5장 정보시스템 구축 관리
    - [ ] 기출문제집
  - [ ] 2024.06.18. 필기 원서 접수
  - [ ] 기본서 이후 기출 문제집 따로 구매하기

---

## 주간 회고

### Liked

- 2달만에 독하게 시작하는 C 프로그래밍을 다 읽었습니다.
- alacritty를 사용하면서 한글입력이 더 자연스러운 것이 좋았습니다.
  - 컬러 문제도 훨씬더 덜합니다. 그래서 테마 설정 문제도 없습니다.
  - 가끔 공백이 2칸 생기는 부분이 조금 아쉬웠습니다. 한글이 2바이트라는 점과 연관이 있을 같다는 추측이 됩니다.
  - tmux를 같이 사용하면 윈도우 이동이 생각보다 쉬워서 좋습니다.
  - 아쉬운 점은 zsh를 사용할 때 자동완성이 없어서 짜로 설정해줘야 한다는 점입니다.

### Learned

- 본인만의 언어 사전을 제거하도록 합니다. 없이 설명하도록 합니다. 다른 직군이든 다른 개발분야든 이런 커뮤니케이션 문제를 제거하고 싶으면 이런 본인만의 사전을 제거하는 것으로 출발해야 합니다.
  - 개념이 다른 개념에 의존해서 벽돌을 쌓는데 최대한 의존을 제거하고 설명하는 것이기 때문에 필요한 방법론입니다.
- 생각보다 사소한 디버깅도 작업을 했다는 내용을 팀에게 알려주도록 합니다.
  - 무엇을 진행했는지 어떤 검증이 필요한지 말하도록 합니다.
- tmux를 사용해서 세션과 윈도우 제어로 alacritty처럼 단순한 터미널에서 이동이 가능합니다.

### Lacked

- 또 확인안 하는 습관이 나왔습니다. 이 습관이 생겨난 이유랑 어떻게 버릴지 알아내야 합니다.
  - 업무를 수행할 때 업무 아이템을 작성할 문서부터 찾는 습관부터 들여야 합니다.
  - 문서를 찾고 업무의 달성기준과 기록을 습관적으로 남겨야 합니다.
- PM은 QA가 아닙니다. 전수 테스트가 필요할 정도로 규모가 크면 도움을 요청할 수 있지만 이런 것도 가끔입니다.
  - PM이 요청한 부분에 대해서 PM이 테스트하는 것은 일반적으로 좋다고 생각합니다. 기능의 부분들을 추가하는 관점하고 유저가 행동하는 흐름이 분명히 다릅니다.

### Longed(잘하기 위해 필요한 것)

- 커뮤니케이션 방법론을 다시 옵시디언에 정리합니다.

### Action Item

- [ ]

---

## 덱 드로우 카운터

- 드로우할 때마다 인덱스를 옮기고 플레이어와 딜러의 패에 쓰기를 하면된다는 생각이 듭니다.
  - 드로우하는 행위를 위해 인덱스 변수가 필요합니다.
  - 플레이어 패, 딜러 패 2개의 문자열을 저장하는 변수가 필요합니다.
  - 플레이어 패와 딜러 패에 쓰기를 하는 동작이 필요합니다.
- 여기서 고민은 드로우하는 행위를 따로 함수로 빼야 하는가?
  - 드로우하는 행위를 따로 두고 사용자의 입력마다 계속 호출하는 방식이 유리할지 고민입니다.

---

- 지금은 엄청 성장한 스타트업의 초기 멤버라는 것을 높이 평가할 필요는 없습니다.
  - 코파운더가 아니면 그렇게 대단한 사람이 아닙니다. 
    - 스타트업에서 초기에 대단한 사람으로 활용하기 위해 기본적으로 대단한 스펙과 능력을 갖고 있었는지 검증해야 합니다. 또 본인 이력이 IR에 있었는지도 알 수 있어야 합니다. 
      - IR 자료에 없는 사람이라면 우리회사에도 없어도 되는 사람입니다.
    - 이런 사항이 해당하는 사람만이 대단한 사람입니다. 이것이 아니면 중소기업 당시 돈줄능력도 부족하고 능력이 별로 없어서 싸게 부려먹던 사람으로 밖에 안 보입니다. 
    - 본인이 뛰어났으면 여러 라운드 동안 함께 했을 것입니다. 
  - 면접관 입장에서 생각은 다릅니다.  회사가 커지면서 능력없는 사람들 짜를 때 같이 짤린 사람으로 밖에 안 보입니다. 
  - 스타트업 다닌다고 그렇게 커리어에 좋은 것은 아닙니다. 
  - 세상 사람들이 인정머리 있을 거라는 착각좀 그만하세요.
- 스타트업을 선택할 때는 굉장히 신중해야 합니다. 스타트업 중 어느 회사를 선택하는 것도 신중해야 하지만 스타트업 분야 자체를 신중히 접근하기 바랍니다.
  - 스타트업이 배민, 쿠팡 이런 회사를 스타트업이라고 착각하는 사람들이 많습니다. 연식 짧은 대기업입니다.
  - 제품을 퇴근하고 만들어보는 단계부터 시리즈 조금 애매하지만 B 라운드까지 스타트업이라고 생각할 수 있습니다.
  - 제일 먼저 본인이 능력이 있는 사람인지 질문해야 합니다.
    - 능력이 있다고 착각하는 것만큼 위험한 것은 없습니다. 퇴근하고 다른 사람들하고 사이드 프로젝트로 본인의 능력을 확인하고 자기객관화부터 해야 합니다.
    - 동료가 능력있다고 하면 사회생활이랑 생존편향을 철저히 무시하는 것입니다.
    - 능력이 없으면 스타트업에서 저임금으로 부려먹히고 짤립니다. 스타트업에서는 평범함으로는 턱없이 부족합니다.
  - 스타트업은 돈이 없어서 싼사람을 씁니다. 스타트업을 다녔다면 당신은 싼 사람으로 밖에 안 보입니다.
- 이런 상황에서 지원자를 검증하는 전략을 생각해볼 수 있습니다.
  - 재직하고 있었을 당시 투자라운드가 어떻게 되나요?
    - 회사에서 기술역량을 중요시 했고 시리즈 A, B에서 신입치고 잘하거나 중고신입이거나 3 ~ 5년차 주니어 엔지니어이고 급여를 높게 줄 생각이었다면 괜찮을 수 있습니다.
    - 시리즈 A미만부터 재직했다면 의심이 필요합니다.
  - 본인은 IR 자료에 포함되어 있고 IR 자료를 우리에게 보여줄 수 있는가?
    - 보여줄 수 없으면 탈락입니다.

