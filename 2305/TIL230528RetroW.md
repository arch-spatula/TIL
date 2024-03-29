# TIL

1일1커밋 무사고: 189일차

04:29

## todo

- [x] 주간회고
- [x] 블로그 릴리즈
  - [x] 블로그 제목 오타 수정

## 주간회고

|  요일  | 시간  |
| :----: | ----- |
| 월요일 | 05:27 |
| 화요일 | 07:13 |
| 수요일 | 00:00 |
| 목요일 | 04:25 |
| 금요일 | 05:26 |
| 토요일 | 00:00 |
| 일요일 | 04:29 |
|   합   | 23:00 |

- [x] 주단위 개발일지 작성하기

- 오늘 블로그 업데이트하면 주단위 개발일지를 올릴 수 있습니다. 하지만 의문은 주단위가 적절한가?
  - 겪은 에러를 자주 정리하고 올리는 것은 좋습니다.

### Liked

- 프로젝트 만들기로 피봇한 선택은 기분 전환에 좋았습니다.
- Deno의 개발 경험이 상당히 좋았습니다.
  - Node를 선수학습하지 않고 Deno를 학습했지만 예상과 다르게 치명적인 문제는 별로 없었습니다.
  - Worker가 없어서 겪은 버그도 있었습니다.
  - Docker, AWS, Github Action의 필요성을 체감할 수 있었습니다.
  - 돌아가는 백엔드까지 작성해도 괜찮기는 합니다. 하지만 좋은 백엔드가 무엇인지 훔쳐배울 수 있습니다.

### Learned

- Deno에는 Worker가 없습니다.
  - Worker는 흥미로운 자바스크립트 객체입니다.
    - 자바스크립트는 싱글 쓰레드인데 브라우저는 멀티쓰레드이고 브라우저의 특성을 활용합니다.
- Deno를 위해 Docker, Github Action, AWS를 공부할 필요가 있습니다.
- VSCode로 인해서 타입스크립트 에러가 발생할 수 있습니다.
  - `moduleResolution: bundler` 문제가 VSCode를 업데이트로 해결했습니다.
- ego를 조심합니다. 새로 합류했다고 무조건 대대적인 개혁을 이룰 필요는 없습니다.
  - 본인 위치에서 잘하는 것부터 시작합니다.
  - 다른 사람들이 어려워하는 것을 해소하기 위해 노력합니다.

### Lacked

- 운동을 별로 안 했습니다. 잡생각이 많아져서 명상으로 해결해 볼 수 있는데 안 했습니다.
- 하루를 4일처럼 사는 방법을 터득해야 합니다. 하지만 하루를 반나절처럼 보내고 있습니다.
  - 이루는 결과가 너무 없기 때문에 그렇습니다.
  - 보상을 여유로 주고 있기 때문에 안 좋은 신호-행위-보상 사이클을 갖고 있습니다.

### Longed(잘하기 위해 필요한 것)

- 운동과 명상이 필요합니다. 잡념을 조절하고 컨디션을 관리해야 합니다.
- 집에서 식사를 그만합니다. 시간 낭비를 너무 많이 합니다.
- 코테, 이력서는 잠시 보류하고 프로젝트 경험을 추가합니다. 더 좋아지고 발전한 코드를 보여줄 수 있도록 해야 합니다.
  - 코테는 감을 잃지 않기 위해 계속하기는 해야 하지만 복습을 잘하기 위해 겪일제 활용하는 전략도 있습니다.
    - 하루는 1시간 복습 자료구조 & 알고리즘 구현
    - 하루는 1시간 이상 혹은 문제 3개 이상 풀기
    - 일요일에는 복습
- 이제 프론트엔드 코드를 작성하기 시작할 수 있습니다. 프론트엔드 코드에 코드 퀄리티 즉 성능말고 관심사를 잘 분리하는 능력을 보여줄 수 있어야 합니다.
  - 디자인 패턴은 싱글튼 말고 다른 패턴들도 보여줄 수 있어야 합니다.
  - 일단은 70% 규칙에 맞게 행동합니다. 처음에는 동작하는 코드 70%를 구현합니다. 어느 정도 동작하면 관심사가 잘 분리되어 있고 테스트하기 좋은 코드로 관심사를 잘 분리합니다.
- 학원에서 특강으로 다루었던 디자인 패턴을 복습해야 합니다. 디자인 패턴을 활용하는 테스트 코드를 작성해봐야 합니다. 자료구조 알고리즘 복습에 더이상 정리할 자료구조 및 알고리즘이 없으면 진행하면 될 것 같습니다.
- 알고있다는 느낌과 알고있는 것을 구분하기 위한 방침을 찾아야 합니다.
  - 지식을 설명할 수 있으면 알고 있는 것입니다.
  - 코드는 테스트코드를 작성할 수 있으면 알고 있는 것입니다.

### Action Item

- [ ] 사이클 20분 월, 수, 금, 일
- [ ] 자료구조 알고리즘 복습 및 추가 월, 수, 금
- [ ] 1일3제 1시간 이하 화, 목, 토

---

[How Partytown allows you to run virtually any JS in the worker thread, in depth](https://www.youtube.com/watch?v=eP6Mti85HeQ)

[Multithreading in Javascript Using Worker Threads](https://www.youtube.com/watch?v=aDqGIhl7cdo)
