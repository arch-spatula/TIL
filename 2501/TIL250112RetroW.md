# AoC 일찍 포기하고 플래시카드 만들기 33일차

1일1커밋 무사고: 762일차

## 감사일기

1. ???

- [x] 주간회고
- [ ] 플래시카드
  - [ ] tag 분류 추가
    - [ ] 무슨 분야로 문제를 낼지 표시
    - [ ] card table에서 분야 설정
  - [ ] 여러 input 추가 
  - [ ] header status code 관례에 맞게 수정
    - 당장 안 해도 괜찮은 로직입니다.
  - [ ] 질문 중복 생성 예외 처리

---

## 주간 회고

### Liked

- 없음.

### Learned

- til을 작성한지 2년을 넘겼습니다.
- 프론트엔드 개발자로서 웹 자체를 전문적으로 다루어야 하는데 여전히 기본기가 너무 약합니다.
- neovim이 가끔 먹통이 될 수 있다는 것도 배웠습니다.
  - tmux랑 다른 window는 영향이 없는 거로 보니 window마다 여러 프로세스를 만들어는 것 같습니다. 그래서 1개가 실패해도 영향이 없는 것 같습니다.
  - `tmux kill-window -t 1`를 이번에 익히게 된 것 같습니다.

### Lacked

- 개인프로젝트에서는 비즈니스 임펙트가 너무 약한 작업에 집중하는 1주일이었습니다.

### Longed(잘하기 위해 필요한 것)

- 문제는 늘 같은데 벗어나는 방법을 모르고 있습니다.

### Action Item

- [ ]

---

## 해시태그 다대다 쿼리 방법

```sql 
SELECT 
    Post.id AS post_id, 
    Post.title AS post_title, 
    GROUP_CONCAT(Hashtag.name) AS hashtags
FROM 
    Post
JOIN 
    PostHashtag ON Post.id = PostHashtag.post_id
JOIN 
    Hashtag ON PostHashtag.hashtag_id = Hashtag.id
GROUP BY 
    Post.id;
```

- 위가 다대다 쿼리 방법이라고 합니다.
- 이런 쿼리를 구현하는데 취업준비 1년 회사경력 1년이나 걸린다는 것을 보면 터무니없는 실력 부족입니다.

```sql 
SELECT * 
  FROM cards_table 
  FULL OUTER JOIN tag_to_card ON cards_table.id = tag_to_card.cardID 
  FULL OUTER JOIN tags_table ON tags_table.id = tag_to_card.tagID
GROUP BY 
    cards_table.id;
```

```sql 
SELECT cards_table.id as id, cards_table.question as question, GROUP_CONCAT(tags_table.name) as tag
  FROM cards_table 
  FULL OUTER JOIN tag_to_card ON cards_table.id = tag_to_card.cardID 
  FULL OUTER JOIN tags_table ON tags_table.id = tag_to_card.tagID
GROUP BY cards_table.id, cards_table.question;
```

```sql 
SELECT 
    cards_table.id as id, 
    cards_table.question as question, 
    GROUP_CONCAT(tags_table.name, '|') as tag, 
    cards_table.nextTry
    FROM cards_table
    FULL OUTER JOIN tag_to_card ON cards_table.id = tag_to_card.cardID
    FULL OUTER JOIN tags_table ON tags_table.id = tag_to_card.tagID
    GROUP BY 
        cards_table.id, 
        cards_table.question, 
        cards_table.nextTry 
    ORDER BY cards_table.nextTry;
```

- 제가 원하는 동작을 대략 구현한 쿼리입니다.
- 위 쿼리를 만들기 위해 1년차 프론트엔드가 검색으로 알아냈습니다. 실력이 엄청나게 문제가 많습니다.
- 4년동안 학교 다녔는데 모르면 당연히 혼나야 합니다. 
- 그리고 국비지원 부트캠프와 취업 준비기간 동안 이런 것도 모르는 것도 당연히 혼나야 할 요소입니다.
- 개발자로서 비슷한 결론을 더 빠르게 도달하는 것이 실력이라고 본다면 엄청나게 실력없는 개발자입니다.

