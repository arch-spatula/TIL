# AoC 일찍 포기하고 플래시카드 만들기 40일차

1일1커밋 무사고: 769일차

## 감사일기

1. ???

- [x] 주간회고
- [x] 주간줍줍
- [ ] 플래시카드
  - [ ] 여러 input 추가 
  - [ ] tag 분류 추가
    - [x] 다대다 쿼리 더 깔끔하게 고치기
    - [ ] 무슨 분야로 문제를 낼지 표시
    - [ ] card table에서 분야 설정
  - [ ] header status code 관례에 맞게 수정
    - 당장 안 해도 괜찮은 로직입니다.
  - [ ] 질문 중복 생성 예외 처리
  - [ ] 단일 정답과 다중 정답 테이블 분리하고 정규화하기
    - [ ] 2개 테이블에 transaction으로 insert 처리

---

## 주간 회고

### Liked

- 오랫만에 운동을 했습니다.

### Learned

- 주간 블로그를 작성해보는 습성이 필요한 것 같습니다.
  - 위키 형식은 피해도 무엇을 달성했는지 기록이 계속 남아야 할 것 같습니다.
- 저는 주변 환경에 영향을 많이 받는 편입니다.

### Lacked

- 유튜브나 드라마를 보는데 개발 관련된 콘텐츠가 줄어느니 취미로 하고 있는 개발도 덜하게 됩니다.

### Longed(잘하기 위해 필요한 것)

- 취미 개발을 위해 개발 시간을 확보하고 개발 콘텐츠를 더 볼 필요가 있습니다.

### Action Item

- [ ] 현실 앱 비슷한 느낌으로 문제를 50개는 더 만들기
- [ ] 플래시카드
  - [ ] 여러 input 추가 
    - 가장 해결할 가치가 높은 문제
    - [ ] 단일 정답과 다중 정답 테이블 분리하고 정규화하기
    - [ ] 2개 테이블에 transaction으로 insert 처리
  - [ ] tag 분류 추가
    - 아래 기능은 후순위로 구현하기.
    - 문제가 너무 많고 특정 분야를 집중하고 싶을 때 사용해야 함.
    - [ ] 무슨 분야로 문제를 낼지 표시
    - [ ] card table에서 분야 설정
  - [ ] header status code 관례에 맞게 수정
    - 당장 안 해도 괜찮은 로직입니다.
  - [ ] 질문 중복 생성 예외 처리

---

## 다대다 테이블 쿼리하기

- 극복해야 할 문제가 생겼습니다.
- 테이블 1개를 쿼리할 때는 비교적 간단하게 구현할 수 있습니다.
- 테이블 2개인데 다대다 관계 쿼리를 구현해야 합니다. 이러한 쿼리를 ORM이 제공하는 기능을 깔끔하게 구현하고 처리하고 싶습니다.

```json
[{
	id: 10,
	name: "Dan",
	posts: [
		{
			id: 1,
			content: "SQL is awesome",
			authorId: 10,
		},
		{
			id: 2,
			content: "But check relational queries",
			authorId: 10,
		}
	]
}]
```

- 저는 위와 비슷하게 다대다 관계를 더 깔끔하게 API 응답으로 반환해야 합니다.
- https://orm.drizzle.team/docs/rqb
  - 예시는 drizzle - ORM에서 찾은 것입니다. 그렇게 어렵게 찾을 것은 아닙니다.

```ts 
  async allCards(): Promise<(Card & { tags: null | string })[]> {
    try {
      const foo = (await this.db.run(`
    SELECT
        cards_table.id as id,
        cards_table.question as question,
        cards_table.answer as answer,
        cards_table.stack as stack,
        cards_table.nextTry as nextTry,
        GROUP_CONCAT(tags_table.name, '|') as tags
        FROM cards_table
        LEFT JOIN tag_to_card ON cards_table.id = tag_to_card.cardID
        LEFT JOIN tags_table ON tags_table.id = tag_to_card.tagID
        GROUP BY
            cards_table.id,
            cards_table.question,
            cards_table.answer,
            cards_table.stack,
            cards_table.nextTry
        ORDER BY cards_table.nextTry;
    `)) as any;
      return foo.rows as (Card & { tags: null | string })[];
    } catch (err) {
      return [];
    }
  }
```

- 거슬렸던 부분은 위 부분입니다.
- `foo`변수명도 거슬리지만 문자열로 저렇게 쿼리하면 나중에 실수할 여지가 많아지기 때문입니다.
  - DB 변경이 있으면 타입스크립트부터 깨져야 유지보수하기 유리할 것이기 때문입니다.

### 기본 설정

- 기본 설정을 다시 건드려야 했습니다.

```ts
import { createClient } from '@libsql/client';
import { Module } from '@nestjs/common';
import { ConfigService } from '@nestjs/config';
import { drizzle } from 'drizzle-orm/libsql';
import * as schema from 'src/db/schema';

@Module({
  providers: [
    {
      provide: 'DATABASE_CONNECTION',
      inject: [ConfigService],
      useFactory: async (configService: ConfigService) => {
        const dbFileName = configService.get('DB_FILE_NAME');
        const client = createClient({ url: dbFileName });
        const db = drizzle({ client, schema });
        return db;
      },
    },
  ],
  exports: ['DATABASE_CONNECTION'],
})
export class DatabaseModule {}
```

- 먼저 위처럼 처리해야 스키마 접근이 가능해집니다.
- `client` 선언을 다시해줘야 했습니다.
- `schema` 정보와 DB 연결정보를 같이 넘겨줘야 합니다. 참고로 타입 선언을 따로 또 해줘야 합니다. 하지만 자동완성은 잘 지원합니다.


```ts
@Injectable()
export class CardsRepository {
  constructor(
    @Inject('DATABASE_CONNECTION')
    private readonly db: LibSQLDatabase<typeof schema> & {
      $client: Client;
    },
  ) {}

  async allCards() {
    try {
      return await this.db.query.cards.findMany({
        with: { tagToCard: { with: { tag: true } } },
      });
    } catch (err) {
      return [];
    }
  }
}
```

- 위처럼 작성하면 맵핑 테이블을 통해서 결국 제가 원하던 다대다 테이블 쿼리가 구현됩니다.
- 막상 하면 그렇게 오래 걸리지 않는데 맞게 구현했는지 알아내기 위한 시행작오가 은근히 있었습니다.

```ts
@Injectable()
export class CardsService {
  constructor(private readonly cardsRepository: CardsRepository) {}

  async findAllCards() {
    const cards = await this.cardsRepository.allCards();
    return cards.map((card) => {
      return {
        id: card.id,
        question: card.question,
        answer: card.answer,
        stack: card.stack,
        cardType: card.cardType,
        nextTry: new Date(card.nextTry).toISOString(),
        tags: card.tagToCard.map((tag) => tag.tag),
      };
    });
  }
}
```

- 서비스 계층에서 쿼리 이후 후처리만 잘 해주면 제가 원하는 깔끔한 응답이 가능해집니다.
- 프론트엔드는 다대다라는 개념을 알고 있어도 받아야 할 정보 자체로 맵핑 테이블의 ID까지 알 필요는 없습니다.
- 그래서 정말 넘겨줄 정보만 넘기는 식으로 해결했습니다.
