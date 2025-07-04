# 자바의 신 읽기 28일차

1일1커밋 무사고: 916일차

## 감사일기

1. ???

- [ ] 주간회고
- [ ] cpp로 만드는 블랙잭
  - [x] 표준입출력 처리하기
    - [x] 표준 입력 구현
- [ ] 데이터 시각화 옵시디언으로 마이그레이션
  - [ ] 비교
    - [x] 양방향 막대 차트(Back-to-back bar chart, Paired Bar chart, Diverging Bar chart)
    - [x] 피라미드 차트(Pyramid chart, Population Pyramid, Age & Sex Pyramid)
    - [ ] 양방향 누적 막대 차트(Diverging Stacked Bar chart)
    - [ ] 범위 차트(Range chart)
    - [ ] 점 차트(Cleveland Dot Plot, Dot Plot)
    - [ ] 연결된 점 차트(Connected Dot Plot, Barbell chart, dumb-bell chart)
  - [ ] 추이
  - [ ] 관계
  - [ ] 위치
  - [ ] 부록

---

## 주간 회고

### Liked

- cpp로 숫자 야구 구현은 LLM의 도움을 받았지만 비교적 쉽게 달성했습니다.
  - 이어서 블랙잭을 만들기 시작할 수 있었습니다.
- 생각한 새로운 것은 아니었지만 비교적 새로운 것들을 많이 배웠습니다.
  - 생각한 새로운 지식은 컴퓨터 과학 새로운 지식을 기대했지만 C++ 문법과 관련된 것들을 더 많이 배웠습니다.
  - 이런 측면에서 주소를 잘못 찾아왔다고 봐야 할 것 같습니다.

### Learned

- cpp이 왜 복잡하다는 다략 알기 시작했습니다.
  - cpp 내부에서 제공해주는 기능이 힙할당을 하는지 스택할당을 제공하는지 매우 의식을 많이 해야 합니다.
  - 네임스페이스를 잘못 사용하면 혼선을 줄 가능성이 높습니다.
- 객체를 다룬다는 점에서 블랙잭을 여러번 다시 만들어 보면서 좋은 형태를 조금식 찾게 되는 것 같습니다.
  - 아니면 최소한 착각을 하고 있습니다.

### Lacked

- 이번주 다이어트는 너무 안했습니다. 식단 관리를 너무 소흘하게 했습니다.
- C++로 블랙잭을 만들면서 이전에 갖고 있던 github 이슈로 개발하는 습관을 그동안 잊고 있었습니다.

### Longed(잘하기 위해 필요한 것)

- 블랙잭에 이슈를 만들고 이슈를 해결하면서 개발을 하면 될 것 같습니다.

### Action Item

- [ ] 블랙잭 만들기
  - [ ] github에 이슈 만들기
  - [ ] 플레이어/딜러 클래스 만들기
  - [ ] 게임 클래스 만들기
  - [ ] 덱 클래스 만들기

---

## cpp 생성자 소멸자 함수 작성하는 방법

```cpp  
class Dog {
public:
    Dog() { std::cout << "Dog 생성\n"; }
    ~Dog() { std::cout << "Dog 소멸\n"; }
};

int main() {
    Dog myDog;  // 스택에 생성
    // 스코프 종료 시 자동 소멸
}
```

- 위는 생성자 함수와 소멸자 함수를 다루고 있습니다.
- 단순하게 파일 분리 없고 선언 위치 구분 없이 구현하고 싶으면 위처럼 구현하면 됩니다.

## 힙은 왜 부하를 만드는가?

- https://www.youtube.com/watch?v=ioJkA7Mw2-U
- WHY IS THE HEAP SO SLOW?
- 스택의 공간은 유한하고 잘못하면 stack overflow 에러를 만들어 낼 수 있습니다.
- 영상에서 주의해야 할 것은 극도로 단순화했다는 것입니다.
- 운영체제의 역할은 어플리케이션에게 자원을 적절히 제공하는 것입니다.
- 시스템콜은 때로는 부하를 만들어냅니다.
  - 운영체제도 결국 소프트웨어라 CPU를 사용해야 합니다. 기존 프로세스의 상태를 저장하고 복원하면서 컨텍스트 스위칭 비용이 발생합니다.
- 당연히 힙할당을 하면 시스템콜을 날려야 합니다. 힙은 시스템 콜을 통해 동적으로 더 많은 자원을 받을 수 있습니다.
- 힙은 예측 불가능한 파편화 문제가 있습니다.
  - 파편화는 반드시 발생하게 되어있습니다.
- 제목이 함정이었는데 힙 자체가 느리지 않고 힙의 파편화 문제를 잘 생각하지 못하고 시스템콜을 많이 날리면 느려지는 것입니다.

