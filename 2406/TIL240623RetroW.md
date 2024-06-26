# 정보 처리기사 준비하기 6일차

1일1커밋 무사고: 559일차

## 감사일기

1. ???

- [x] 주간줍줍
- [x] 주간회고
- [ ] 소프트웨어 1 ~ 5장
  - [x] 오늘 시도
  - [ ] 1장 소프트웨어 설계
    - [x] 화면 설계
      - [x] 품질 요구사항
      - [x] UI 상세 설계
      - [x] HCI / UX / 감성공학
      - [x] 요약 읽기
    - [ ] 애플리케이션 설계
      - [x] 소프트웨어 아키텍쳐
      - [x] 아키텍쳐 패턴
      - [x] 객체지향
      - [ ] 모듈
      - [ ] 공통 모듈
      - [ ] 코드
      - [ ] 디자인 패턴
      - [ ] 요약 읽기
    - [ ] 인터페이스 설계
      - [ ] 시스템 인터페이스 요구사항 분석
      - [ ] 인터페이스 요구사항 검증
      - [ ] 인터페이스 방법 명세화
      - [ ] 미들웨어 솔루션 명세
      - [ ] 요약 읽기
  - [ ] 2장 소프트웨어 개발
    - [ ] 데이터 입출력 구현
    - [ ] 통합 구현
    - [ ] 제품 소프트웨어 패키징
    - [ ] 애플리케이션 테스트 관리
    - [ ] 인터페이스 구현
  - [ ] 3장 데이터베이스 구축
    - [ ] 논리 데이터베이스 설계
    - [ ] 물리 데이터베이스 설계
    - [ ] SQL 응용
    - [ ] SQL 활용
    - [ ] 데이터 전환
  - [ ] 4장 프로그래밍 언어 활용
    - [ ] 서버 프로그램 구현
    - [ ] 프로그래밍 언어 활용
    - [ ] 응용 SW 기초 기술 활용
  - [ ] 5장 정보시스템 구축 관리
    - [ ] 소프트웨어 개발 방법론 활용
    - [ ] IT프로젝트 정보 시스템 구축 관리
    - [ ] 소프트웨어 개발 보안 구축
    - [ ] 시스템 보안 구축
  - [ ] 기출문제집
    - [ ] 1회
      - [ ] 문제 풀이
      - [ ] 오답노트
    - [ ] 2회
      - [ ] 문제 풀이
      - [ ] 오답노트
    - [ ] 3회
      - [ ] 문제 풀이
      - [ ] 오답노트
    - [ ] 4회
      - [ ] 문제 풀이
      - [ ] 오답노트
    - [ ] 5회
      - [ ] 문제 풀이
      - [ ] 오답노트
    - [ ] 6회
      - [ ] 문제 풀이
      - [ ] 오답노트
    - [ ] 7회
      - [ ] 문제 풀이
      - [ ] 오답노트
    - [ ] 8회
      - [ ] 문제 풀이
      - [ ] 오답노트
    - [ ] 9회
      - [ ] 문제 풀이
      - [ ] 오답노트
    - [ ] 10회
      - [ ] 문제 풀이
      - [ ] 오답노트
- [ ] 기본서 이후 기출 문제집 따로 구매하기
- [ ] 2024년 07월 25일 (목) 08:40 호서대학교 천안캠퍼스 1호관3층 CBT 3실(305호)에 정보처리기사 필기 시험 보기
- [ ] 플래시 카드 2.0 서비스 만들기
  - [ ] nuxt 설치
  - [ ] mongoose ORM 설치
  - [ ] vercel 배포
  - [ ] 로그인 구현
  - [ ] 어드민 전용기능(배치 삭제, 생성 제한)
  - [ ] 핀터레스트 레이아웃 구현
  - [ ] 문제 유형 태그 구현
  - [ ] 카나리 설정
- [ ] go 언어 공식문서 복습
  - https://go.dev/tour/methods/23
  - 메서드 지식문제가 아니라 인코딩 디코딩에 대한 지식이 없는 문제로 보입니다.
- [ ] go 언어 숫자야구
  - [ ] 난수 3개 생성
- [ ] go 언어 TDD 문서
- [ ] go 언어 블랙잭
- [ ] TIL-CLI 1.0.1
  - [ ] json 파일 다시 설정
  - [ ] 입력 설계
  - [ ] 테스트 설계
  - [ ] 입력 - 처리 - 출력 mvc 패턴 구축
  - [ ] 실행파일 별칭 지정
- [ ] neovim 회사에서 사용가능하게 만들기

---

## 주간 회고

### Liked

- 회사에서 룩업 테이블 패턴이 유용하게 사용되었습니다.
  - 성능개선에 해당하는 기여를 했습니다. 이력서에 넣기에는 너무 기본적인 것이라 해도 되는 것인지는 모르겠습니다.
- 정보처리기사 시험 등록을 했습니다. 퇴근하고 집중할 것이 생겼습니다. 또 너무 부족한 CS 지식 기본기를 학습할 수단이 생겼습니다.

### Learned

- v-if, v-show를 조건부로 처리하는 것이 가능합니다. 디렉티브 추가 자체는 조건부로 못해도 상태와 반응은 조건부로 갖도록 만들 수 있습니다.
- 옵시디언으로 회사에서 한 활동과 줍줍한 링크를 먼저 옮겨두고 회고하는 것이 더 효과적입니다.
- 정보처리기사 내용을 공부하면서 제가 살고 있는 세계가 다르다는 것을 알았습니다.
  - 대부분의 회사는 스타트업이 보기에는 레거시 시스템입니다. 드림위버 같은 소프트웨어를 사용 안합니다. 하지만 이것은 스타트업 관점입니다. 신규 프로젝트할 때 고집할 이유는 실무자 본인의 익숙함말고 없습니다.

### Lacked

- 정보처리기사 학습 속도가 너무 느립니다. 이번주면 거의다 끝나야 하는데 이제 객체지향을 시작합니다.
  - 천천히 하는 것은 게으른 것입니다. 그렇게 어려운 개념도 아닌데 오래해야 한다는 것은 그만큼 기본기 없다는 것입니다.
  - 정보처리기사 자격증을 공부하기 위해 가장 많은 진도는 어제였는데 기회를 잘 활용하지 않았습니다.
  - 18/156 정도 달성했습니다. 약 11% 정도 읽기를 한 것입니다.
    - 최소한 3회독을 해야 합니다. 그 후에는 효율을 높이기 위해서 플래시카드를 자체적으로 만들어야 합니다. 그리고 기출문제집을 최소한 2주 전부터 풀기 시작해야 합니다. 하지만 가족 여행도 일정에 포함되어 있습니다. 
  - 시간이 없다는 것을 자각해야 합니다.

### Longed(잘하기 위해 필요한 것)

- 1회독을 빠르면서 꼼꼼하게 봐야 합니다. ~~트레이드 오프가 없다는 것은 엔지니어가 별로 안 좋아하는 말이지만~~
- 주말에는 해보고 싶은 프로그래밍을 해볼 생각을 했는데 시간이 많이 부족할 것입니다.
  - 갖고 놀 장난감이 많다고 볼 수 있지만 사치라는 것을 자각해야 합니다. 지금은 Nix나 neovim 갖고 장난칠 시기가 아닙니다.

### Action Item

- [ ] 소프트웨어 1 ~ 5장
  - [ ] 1장 소프트웨어 설계
    - [ ] 애플리케이션 설계
      - [ ] 모듈
      - [ ] 공통 모듈
      - [ ] 코드
      - [ ] 디자인 패턴
      - [ ] 요약 읽기
    - [ ] 인터페이스 설계
      - [ ] 시스템 인터페이스 요구사항 분석
      - [ ] 인터페이스 요구사항 검증
      - [ ] 인터페이스 방법 명세화
      - [ ] 미들웨어 솔루션 명세
      - [ ] 요약 읽기
  - [ ] 2장 소프트웨어 개발
    - [ ] 데이터 입출력 구현
    - [ ] 통합 구현
    - [ ] 제품 소프트웨어 패키징
    - [ ] 애플리케이션 테스트 관리
    - [ ] 인터페이스 구현
  - [ ] 3장 데이터베이스 구축
    - [ ] 논리 데이터베이스 설계
    - [ ] 물리 데이터베이스 설계
    - [ ] SQL 응용
    - [ ] SQL 활용
    - [ ] 데이터 전환
  - [ ] 4장 프로그래밍 언어 활용
    - [ ] 서버 프로그램 구현
    - [ ] 프로그래밍 언어 활용
    - [ ] 응용 SW 기초 기술 활용
  - [ ] 5장 정보시스템 구축 관리
    - [ ] 소프트웨어 개발 방법론 활용
    - [ ] IT프로젝트 정보 시스템 구축 관리
    - [ ] 소프트웨어 개발 보안 구축
    - [ ] 시스템 보안 구축
  - [ ] 기출문제집
    - [ ] 1회
      - [ ] 문제 풀이
      - [ ] 오답노트
    - [ ] 2회
      - [ ] 문제 풀이
      - [ ] 오답노트
    - [ ] 3회
      - [ ] 문제 풀이
      - [ ] 오답노트
    - [ ] 4회
      - [ ] 문제 풀이
      - [ ] 오답노트
    - [ ] 5회
      - [ ] 문제 풀이
      - [ ] 오답노트
    - [ ] 6회
      - [ ] 문제 풀이
      - [ ] 오답노트
    - [ ] 7회
      - [ ] 문제 풀이
      - [ ] 오답노트
    - [ ] 8회
      - [ ] 문제 풀이
      - [ ] 오답노트
    - [ ] 9회
      - [ ] 문제 풀이
      - [ ] 오답노트
    - [ ] 10회
      - [ ] 문제 풀이
      - [ ] 오답노트
- [ ] 기본서 이후 기출 문제집 따로 구매하기
- [ ] 2024년 07월 25일 (목) 08:40 호서대학교 천안캠퍼스 1호관3층 CBT 3실(305호)에 정보처리기사 필기 시험 보기
- [ ] 플래시 카드 2.0 서비스 만들기
  - [ ] nuxt 설치
  - [ ] mongoose ORM 설치
  - [ ] vercel 배포
  - [ ] 로그인 구현
  - [ ] 어드민 전용기능(배치 삭제, 생성 제한)
  - [ ] 핀터레스트 레이아웃 구현
  - [ ] 문제 유형 태그 구현
  - [ ] 카나리 설정
- [ ] go 언어 공식문서 복습
  - https://go.dev/tour/methods/23
  - 메서드 지식문제가 아니라 인코딩 디코딩에 대한 지식이 없는 문제로 보입니다.
- [ ] go 언어 숫자야구
  - [ ] 난수 3개 생성
- [ ] go 언어 TDD 문서
- [ ] go 언어 블랙잭
- [ ] TIL-CLI 1.0.1
  - [ ] json 파일 다시 설정
  - [ ] 입력 설계
  - [ ] 테스트 설계
  - [ ] 입력 - 처리 - 출력 mvc 패턴 구축
  - [ ] 실행파일 별칭 지정
- [ ] neovim 회사에서 사용가능하게 만들기


