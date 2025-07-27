# 블로드 다시 만들기 27일차

1일1커밋 무사고: 958일차

## 감사일기

1. ???

- [x] 주간회고
- [ ] 블로그 다시 만들기 전 실험
  - [ ] 검색 만들기
  - [ ] ToC
- [ ] 데이터 시각화 옵시디언으로 마이그레이션
  - [ ] 위치
    - [x] 등고선 지도(Contour map, lsarithmic map, Isochrone map, Isopleth map)
    - [ ] 연결 지도(Connection map, Link map)
    - [ ] 이동 경로 지도(Route map)
    - [ ] 흐름 지도(Flow map)
    - [ ] 카토그램(Cartogram)
    - [ ] 돌링 카토그램(Dorling Cartogram, Dorling map)
    - [ ] 타일 격자 지도(Tile Grid map, Grid map, Equal-area cartogram)

---

## 주간 회고

### Liked

- 개발자 블로그를 다시 만들기 전 실험을 하고 있는데 많은 부분이 된 것으로 보이고 있습니다.
  - 이번에 개발자 블로그 다시 만들기를 시도할 때는 글을 작게 여러개 올릴까 합니다.

### Learned

- vite가 preview랑 dev랑 다르게 동작하는데 dev는 타입스크립트 파일을 받아서 처리하는 것을 알게되었습니다.
  - preview는 rollup이 번들링해서 처리된 결과를 볼 수 있게 됩니다.

### Lacked

- 체중관리의 목표에 있어서는 이번주는 쉬었습니다. 아마 다음주까지 잠시 쉬고자 합니다.
- 이번에 기대한 하던 트레바리는 중간에 취소 되었습니다.
  - 이제 환불요청하고 새롭게 시도해볼 트레바리 모임을 찾아봐야 합니다.
- EChart를 LLM으로 업무를 했습니다. 그것도 많은 로직을 LLM에게 작게 쪼개서 시켜보니까 성과가 꽤 괜찮았습니다.
  - 반대로 제가 직접 만들 수 있었어야 하는 로직을 LLM보다 떨어지는 능력을 갖고 있는 것을 확인했습니다.

### Longed(잘하기 위해 필요한 것)

- 퇴근하고 어려운 문제를 풀어보는 연습을 해야 합니다.
  - EChart를 활용하든 어떤 데이터 시각화가 되었든 어려운 표현을 클라이언트 개발자로 할 수 있어야 합니다.
  - 어려운 개발을 잘 하지 못했던 것은 그동안의 태만의 결과입니다.
- 블로그 만들기 전 실험을 빠르게 마무리 지어야 합니다.
  - 검색, 태그, ToC 등 끝내고 다른 작업을 알아보기 시작해야 합니다.

### Action Item

- [ ] 블로그 다시 만들기 전 실험
  - [ ] 검색 만들기
  - [ ] ToC
- [ ] 데이터 시각화 옵시디언으로 마이그레이션
  - [ ] 위치
    - [x] 등고선 지도(Contour map, lsarithmic map, Isochrone map, Isopleth map)
    - [ ] 연결 지도(Connection map, Link map)
    - [ ] 이동 경로 지도(Route map)
    - [ ] 흐름 지도(Flow map)
    - [ ] 카토그램(Cartogram)
    - [ ] 돌링 카토그램(Dorling Cartogram, Dorling map)
    - [ ] 타일 격자 지도(Tile Grid map, Grid map, Equal-area cartogram)

---

## 브라우저 새로고침 혹은 창닫기 이벤트에 접근하기

- vue의 beforeUnmount 라이프사이클을 어떻게 흉내낼 수 있는지 의문이었습니다.
  - 직접 소스코드를 통해서 파악한 것은 아닙니다.

```ts
window.addEventListener("beforeunload", () => {});
```

- https://developer.mozilla.org/ko/docs/Web/API/Window/beforeunload_event
  - 이벤트는 위에 작성되어 있습니다.
