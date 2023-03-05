1일1커밋 무사고: 111일차

```css
@import url("https://fonts.googleapis.com/css?family=Raleway:200");

html,
body {
  height: 100%;
}
body {
  display: flex;
  justify-content: center;
  align-items: center;
  height: 100%;
  background: #1d1f20;
}
#box {
  display: flex;
  align-items: center;
  justify-content: center;
  width: 400px;
  height: 200px;
  color: white;
  font-family: "Raleway";
  font-size: 2.5rem;
}
.gradient-border {
  --borderWidth: 3px;
  background: #1d1f20;
  position: relative;
  border-radius: var(--borderWidth);
}
.gradient-border:after {
  content: "";
  position: absolute;
  top: calc(-1 * var(--borderWidth));
  left: calc(-1 * var(--borderWidth));
  height: calc(100% + var(--borderWidth) * 2);
  width: calc(100% + var(--borderWidth) * 2);
  background: linear-gradient(
    60deg,
    #f79533,
    #f37055,
    #ef4e7b,
    #a166ab,
    #5073b8,
    #1098ad,
    #07b39b,
    #6fba82
  );
  border-radius: calc(2 * var(--borderWidth));
  z-index: -1;
  animation: animatedgradient 3s ease alternate infinite;
  background-size: 300% 300%;
}

@keyframes animatedgradient {
  0% {
    background-position: 0% 50%;
  }
  50% {
    background-position: 100% 50%;
  }
  100% {
    background-position: 0% 50%;
  }
}
```

https://codepen.io/mike-schultz/pen/NgQvGO

https://css-tricks.com/animating-a-css-gradient-border/

https://codepen.io/a3k5/pen/MWjZpjg

html에 그레이디언트 재량은 별로 없습니다.

# todo

- [ ] 주간 회고

# 주간회고

- [ ] 프론트엔드 면접질문 하루 1개
- [ ] 수료 전까지는 자료구조 & 알고리즘 강의 하루 1강

- 지난주 목표였습니다. 모두 시간이 없습니다. 물론 휴일이 껴있는 수요일과 오늘은 하루를 즐겁게 보내기로 했습니다.
  프론트엔드 면접질문 1개를 매일 작성하기보단 수료 이후 매일 3개를 정리하면 1달에 100개를 커버할 수 있고 6개월에 대부분 대표적인 질문을 커버할 수 있을 것 같습니다.
- 자료구조 & 알고리즘도 수료하고 난 뒤에 해도 늦지 않을 것입니다. IT 시장이 불황이라 채용이 어려울 수 밖에 없으면 먼저 코테를 위한 응용지식 핵심만 빠르게 보고 로우레벨 CS 지식과 C언어부터 천천히 보면 될 것 같습니다. 금방 취업에 성공하는 게 이상할 것이라는 것을 알고 있습니다. 자바스크립트를 활용한 코테 강의와 튜토리얼 2개를 보고 수료 이후 매일 6개월간 3문제를 풀면 될 것이라고 알고 있습니다.
- 혼자할 프로젝트는 모노리포 전략을 활용한 플레시카드를 만들까 고민입니다. 사실 고민보단 이미 마음에 담아 뒀습니다.

## Liked

- 중간에 휴일이 껴있어서 환기가 되었습니다.
- 토요일과 일요일에 블로그를 더욱더 많이 개발했습니다. 목록 카드와 코드 블럭을 만들었습니다. Cook-Book을 열심히 뽑기 시작해도 됩니다. 이제 댓글 기능을 추가하면 포트폴리오 가치가 보입니다.

## Learned

- supabase에 타입지정하는 법을 배웠습니다. 개인 프로젝트를 위해 결재할 수 있을 때 더욱더 본격적으로 활용할 수 있을 것 같습니다.
- 중요한 리소스 중 하나는 의욕입니다. 어떤 호기심이 생기고 호기심을 충족하기 위한 활동을 하는 것도 중요합니다. 가장 지식을 얻는 효율이 좋습니다. 단점은 호기심이 생기는 것과 실제 필요한 지식이 불일치 할 수 있습니다. 한국 정서에 굉장히 안 좋지만 업무가 없는 날에는 충분히 호기심을 충족하면서 성장해도 된다고 생각합니다. 물론 단기적으로는 성장이 없습니다. 그냥 건전한 오락 혹은 취미가 맞습니다. 휴일은 휴식하고 충천하는 것이 목적입니다. 물론 우리나라 정서상 휴일도 당연히 업무일 입니다.
- 나중에 라이브러리를 만들고 문서화가 필요하면 `docusaurus`를 활용할 것입니다. astro는 로우레벨로 설정할 수 있는 것이 많지만 문서화 문제를 더욱더 효율적으로 해결하고 설정이 덜 필요한 `docusaurus`가 좋을 것이라고 추측됩니다.
- 개발자가 테스크를 잘개 쪼게는 것은 대부분의 업무상 이점이 많습니다. 업무상 중복이 발생했을 때 중복작업과 merge conflict가 발생할 수 있습니다. 잘 쪼개지면 중복이 덜 발생합니다. 단점은 관리비용입니다. 이슈를 만들고 추가하고 문서업무 비중이 증가합니다.
- Cookbook의 의미는 레시피를 실천하면서 무언가를 만드는 프로그래밍 학습자료입니다. 알게 된 것을 대충 쑤셔박는 방식으로 작성했습니다. 물론 나중에 다시 볼 때가 많았습니다. 하지만 나중에 미래의 자신에게 모르는 것을 다시 가르쳐줘야 할 때 효율이 떨어질 것 같습니다.

## Lacked

- 프로젝트 1주일 남았는데 너무 몰입을 덜 했습니다.
- 해결한 문제보다 만든 문제가 더 많았습니다. 디자인적인 수정과 기능적인 수정 중간에 새로운 버그들이 많이 발생했습니다.
- 시간이라는 리소스가 부족했습니다. 본격적인 디자인이 1주일 정도 늦게 적용시킬 수 있었습니다.
- 걱정과 잡념이 많아 집중력이 부족했던 한주였습니다.
- 매일매일 다음날 무엇을 할지 정해야 하는데 이런 것을 안 했습니다. 그러먼서 무엇을 해야할지 정하기 어려웠습니다. 다음날 목표를 정하는 것이 확실히 더 효율적일 것 같습니다.

## Longed(원하는 것)

- 잡념, 걱정, 집중력 부족은 운동부족과 연결된 것 같습니다. 수료 이후 매일 사이클을 탈 것입니다. 유산소 운동을 하면서 체력을 유지할 것입니다.
- 포트폴리오로 개발자 블로그를 마무리하고 싶어졌습니다. 코드 블럭과 목록 카드를 만들고 보람을 느꼈습니다. 블로그 만들기를 위해 다른 부분들도 진행하고 싶습니다.
- deno fresh를 설치해보고 이름처럼 신선하다는 생각이 들었습니다. 프론트엔드와 백엔드가 연결된 프로젝트를 굉장히 빠르게 프로토타이핑하기 좋아 보였습니다.
- 꾸준한 면접 연습을 위해 개발자 이력서를 만들고 싶습니다. 하지만 저의 장점을 파악하기 어렵습니다.

## Action Item

- [ ] 이번주 잘 마무리하기
- [ ] 수료이후 계획 새우기
  - [ ] 스터디 모집과 진행 계획 세우기
    - [ ] 코테 준비
    - [ ] 면접 질문 & CS 지식
    - [ ] 사이드 프로젝트
    - [ ] 영어공부 계획(영단어, 영타, 영작)
