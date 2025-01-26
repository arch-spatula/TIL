# AoC 일찍 포기하고 플래시카드 만들기 47일차

1일1커밋 무사고: 776일차

## 감사일기

1. ???

- [ ] 주간회고
- [x] 주간줍줍
- [ ] 플래시카드 50개 추가하기
- [ ] 플래시카드
  - [ ] 여러 input 추가 
    - 브랜치명: feat/multiple-answers
    - 가장 해결할 가치가 높은 문제
    - [ ] 단일 정답과 다중 정답 테이블 분리하고 정규화하기
      - [ ] 갱신 transaction 처리하기
        - [ ] 단일 정답 복수 정답 보여주기
        - [ ] 갱신 대상 전략패턴으로 구분 처리
  - [ ] tag 분류 추가
    - 아래 기능은 후순위로 구현하기.
    - 문제가 너무 많고 특정 분야를 집중하고 싶을 때 사용해야 함.
    - [ ] 무슨 분야로 문제를 낼지 표시
    - [ ] card table에서 분야 설정
  - [ ] header status code 관례에 맞게 수정
    - 당장 안 해도 괜찮은 로직입니다.
  - [ ] 질문 중복 생성 예외 처리
  - [ ] 현실 앱 비슷한 느낌으로 문제를 50개는 더 만들기



---

## 주간 회고

### Liked

-

### Learned

- 동적으로 늘어난 input에 대해서 `v-model`을 어떻게 적용해야 하는지 당황했습니다. 하지만 결국 해결책을 찾았습니다.

### Lacked

- 주중에는 시간이 없지만 주말에는 시간이 많아도 활용을 별로 하지 않았습니다. 이미 본 드라마를 굳이 다시 돌려본게 시간을 많이 낭비했습니다.

### Longed(잘하기 위해 필요한 것)

-

### Action Item

- [ ]


---

```vue 
<script setup lang="ts">
const multipleAnswers = ref<string[]>(['']);
</script>
<template>
  <div
    v-for="(multipleAnswer, idx) in multipleAnswers"
  >
    <TextInput
      :key="idx"
      v-model="multipleAnswers[idx]"
      class="input"
      placeholder="예: Central Processing Unit"
    />
  </div>
</template>
```
