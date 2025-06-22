# C++로 블랙잭 7일차

1일1커밋 무사고: 923일차

## 감사일기

1. ???

- [x] 주간회고
- [ ] 책상 구매
- [ ] cpp로 만드는 블랙잭
  - [ ] 게임 클래스 만들기
    - [ ] 초기 배당구현을 위해 난수로 승패 정하기
    - [ ] 베당 구현
  - [ ] 덱 클래스 만들기
- [ ] 데이터 시각화 옵시디언으로 마이그레이션
  - [ ] 비교
    - [x] XY 히트맵(XY Heat map, Heat map)
    - [x] 레이더 차트(Radar Chart, star chart, spider diagram, web chart)
    - [ ] 폴라 차트(Polar Chart, Coxcomb polt, polar area plot)
  - [ ] 추이
    - [ ] 선 차트(Line Chart)
    - [ ] 영역 차트(Area Chart)
    - [ ] 누적 영역 차트(Stacked Area Chart)
    - [ ] 팬 차트(Fan Chart)
    - [ ] 범프 차트(Bump Chart)
    - [ ] 경사 차트(Slope Chart)
    - [ ] 주가 차트(Stock Price Chart, One-high-low-close chart(OHLC chart), Price chart, Candlestick chart)
    - [ ] 폭포 차트(Waterfall chart)
    - [ ] 타임라인 차트(Timeline chart, Range chart, gantt chart)
    - [ ] 연결된 산점도(Connected Scatter Plot)
    - [ ] 방사형 선 차트(Radial Line Chart, Cricular Line Chart, Polar Line Chart)
  - [ ] 관계
  - [ ] 위치
  - [ ] 부록

---

## 주간 회고

### Liked

- 이번주에는 그동안 안해봤던 모각에 오랜만에 나갔습니다.
  - 보통은 회사에 비밀로 해야 하는 것입니다. 회사 밖으로 겉도는 것으로 보이기 때문입니다.

### Learned

- 이번주는 지금이 아닌 다른 곳도 상당히 힘들다는 것을 배웠습니다.
  - 회사에서 고객사에 파견나가 있는 곳들은 그렇게 편하지 않다는 것을 알게되었습니다. 오히려 상당히 이상하다는 것을 배웠습니다.
    - 같이 일해볼 수 없었지만 대화를 해보면서 개발자로서 교양이 풍부한 사람이 그런 곳에 투입이 되었다는 것이 마음에 걸렸습니다. 아마 더 좋은 대우를 받아야 할 사람이 안 좋은 대우를 받고 있다는 것입니다.
- C++로 블랙잭을 만들어가면서 배우는 것이 컴퓨터의 디테일을 알아가는 것보다 C++이라는 언어를 알아는 것이 더 많은 것 같습니다.
  - 로우레벨 컨트롤을 더 할 수 있다고 하는데 아직 그정도로 챙겨야할 수준은 아닙니다.
- 건강상 허리랑 어깨는 생각보다 큰 이슈는 아니었던 것입니다.
  - 정형외과를 방문해보니 물리치료가 생각보다 병원장비로 안마의자의 안마 받는 것이랑 비슷했던 것 같습니다.
  - 모니터를 더 높게 두고 목스트레칭을 더 자주 해야 합니다.
  - 의외로 등근육들을 발달시키라고 했습니다.
    - 척추가 완전히 좌우 중간에 올 수 없어도 어느정도 예방하고 점점 중앙으로 오게 만들기 위해서는 등근육을 전반적으로 발달시키라고 했습니다.
  - 휴대폰 사용이 어깨의 주된 원인이라고 보입니다. 어깨가 말리면서 솔뎌 프레스할 때 뼈가 부딪치는 느낌을 받았습니다.
    - 어깨 근육을 강화해야 하는 것은 맞지만 뼈에 그런 자극이 생기면 오히려 중단하라고 했습니다.

### Lacked

- 이번주에는 내과에서 신장검사를 못했습니다. 주말 병원은 생각보다 사람이 많았습니다.

### Longed(잘하기 위해 필요한 것)

- 건강관리에 계속 신경을 써야 합니다.
- 슬슬 블랙잭을 마무리하고 코테 공부와 CS지식 공부에 전념해서 이직준비를 해야 합니다.
  - 한편으로는 웹 개발에 전념하는 것이 더 필요할 것 같기도 합니다. 어느정도 복잡성이 높고 수준이 높은 어플리케이션을 개인적으로 개발해야 하는데 전혀 안 하고 있었습니다.

### Action Item

- [ ] 책상 구매
- [ ] cpp로 만드는 블랙잭
  - [ ] 게임 클래스 만들기
    - [ ] 초기 배당구현을 위해 난수로 승패 정하기
    - [ ] 베당 구현
  - [ ] 덱 클래스 만들기
- [ ] 데이터 시각화 옵시디언으로 마이그레이션
  - [ ] 비교
    - [ ] 폴라 차트(Polar Chart, Coxcomb polt, polar area plot)
  - [ ] 추이
    - [ ] 선 차트(Line Chart)
    - [ ] 영역 차트(Area Chart)
    - [ ] 누적 영역 차트(Stacked Area Chart)
    - [ ] 팬 차트(Fan Chart)
    - [ ] 범프 차트(Bump Chart)
    - [ ] 경사 차트(Slope Chart)
    - [ ] 주가 차트(Stock Price Chart, One-high-low-close chart(OHLC chart), Price chart, Candlestick chart)
    - [ ] 폭포 차트(Waterfall chart)
    - [ ] 타임라인 차트(Timeline chart, Range chart, gantt chart)
    - [ ] 연결된 산점도(Connected Scatter Plot)
    - [ ] 방사형 선 차트(Radial Line Chart, Cricular Line Chart, Polar Line Chart)
  - [ ] 관계
  - [ ] 위치
  - [ ] 부록
