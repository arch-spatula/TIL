# TIL

06:54

## todo

- [x] Navbar 라우팅
- [x] 페이지 컴포넌트 만들기
- [x] 플래시카드 mocking 경고
- [x] 1일3제 1시간 이하
- [x] 월간회고
- [x] 명상

## 월간회고

- 지난 달 달성한 것을 확인해봅시다. 그리고 달성이 만드는 결과를 봅시다.

  - 블로그 astro에서 docusaurus로 마이그레이션에 성공했습니다.
    - 이전보다 블로그에 더 글을 많이 작성하기 시작했습니다.
    - 블로그에 다루고 싶은 주제를 이슈로 만들고 생각하는 시간을 시간을 갖을 수 있게 되었습니다.
    - 개별 레포로 분야를 분리하는 부담에서 자유로워 질 수 있게 되었습니다. 새로운 분야 관심사 분리가 필요한 글을 따로 정리하기 쉬워졌습니다.
    - velog에서 작성한 내용은 아직도 정리하고 있습니다. 복습을 생각하면서 자료를 이동시키고 있습니다.
  - 플래시카드 풀스택 프로젝트를 시작했습니다.
    - 레포를 만든 것은 05월 17일이지만 05월 25일부터 본격적인 작업에 착수했습니다. 배포는 28일에 했습니다.
    - API를 교육과정 강의자료와 무관하게 만들 수 있는 경험을 했습니다. API로 db에 CRUD를 할 수 있는 수준까지 작성하게 되었습니다.
  - 모노레포 적용방법
    - 모노레포 코드베이스에서 대부분 명령은 root에서 내려야 한다는 것을 알게 되었습니다.
    - AWS, github action를 학습할 필요가 생겼습니다.
  - <리팩토링> 읽기
    - 꽤 많은 프로그래머들이 리팩토링을 실천합니다. 당장 코드 퀄리티가 너무 안 좋다고 낙담할 필요가 없습니다.
    - 리팩토링 도서도 결국 패턴을 다루지만 변형을 가하는 과정을 다루는 패턴입니다.
  - 자료구조 알고리즘을 복습할 수 있는 시스템을 만들었습니다.
    - 코테 문제에 이전보다 어려운 문제를 어떻게 풀어야 하는지 더 잘 보이게 되었습니다.
    - Stack, Queue, hash를 활용하는 문제를 풀 수 있게 되었습니다.

- 2분기 계획에서 무엇을 달성했는지 확인해봅시다.

  - 이력서 초안 작성하기
    - 이력서 초안이 작성되었지만 부족합니다. 담당한 역할과 비즈니스적인 기여로 어떻게 문제를 해결했는지에 대한 내용이 별로 없습니다.
    - 40개 원티드 기업에 지원하고 1개의 합격을 받았다는 것은 그만큼 이력서가 부족하다는 것으로 파악할 수 있습니다.
  - 장기 CS 지식은 면접질문 답하면서 학습하게 되었습니다.
  - 지원, 면접 경험은 있습니다. 하지만 코테 경험이 없습니다.
    - 이력서가 완성되어야 코테 경험을 할 수 있습니다.
  - 팀 프로젝트 포트폴리오로 정리하기는 안 했습니다.
    - 포트폴리오 프로젝트 2개만 있기 때문에 비효율적입니다.
    - 개인 프로젝트 1개 더 추가하도록 합니다.
  - 유데미 완강은 4월에 했습니다.
    - 완강하고 추가적으로 복습해보면서 더 좋은 학습자료와 비교하고 다시 작성하는 것이 필요하다는 생각이 들었습니다.
    - 유튜브 자료구조 알고리즘 완강은 할 필요가 없습니다. 겹치는 내용을 복습한다는 접근은 좋지만 이미 알고 있는 이론을 다시 복습할 필요는 없습니다.
  - CS 지식은 달성한 것이 없습니다.
    - 컴퓨터 역사, 이산수학, 컴퓨터 구조론, 운영체제론, 네트워크, 데이터베이스 이론, 보안, 컴파일러, 독하게 시작하는 C 프로그래밍 완독 이룬 것이 아무것도 없습니다.
    - 보류하는 것이 가치가 더 높은 것을 정하는 것이기 때문에 지금 시점에서는 적절합니다. 면접에서 CS 지식 때문에 떨어진다는 것을 검증하면 그때 시작해도 늦지 않습니다.

### Liked

- 5월이 지나고 얻은 것은 막혔던 방향에서 새로운 길을 찾았습니다. 단순 구현이 방향이었는데 지금은 계층분리, 관심사 분리가 주된 관심입니다. 동작이 동일해도 무엇이 더 좋은 코드인지 일반적인 방향이라도 얻었습니다.
  - 계층을 분리한다는 것은 가장 큰 틀에서 MVC로 리액트의 JSX를 View로 사용하고 View에 custom hook으로 이벤트를 주입하고 이벤트를 통해서 Model인 State, date를 class로 제어하는 것입니다.
  - 생각보다 작은 조언이 유용했습니다. 객체리터럴을 사용하지 않고 todo-app을 리액트로 만들면 Model이 클래스로 분리할 수 있다. 또 메서드로 갱신을 어떻게 처리하는지 은닉하는 것도 가능합니다.
- 테스트 코드를 작성하는 방향을 얻었습니다. 단위 테스트를 잘 작성하고 싶어졌습니다. 리팩토링에 중요한 전 작업을 하기 위해 필요합니다.

### Learned

- 기초의 방향에서 대서 얻었습니다. 지금 시점에서 기초에 대한 방향은 관심사의 분리입니다. 효과적으로 관심사를 분리하고 코드를 정리할 수 있는 스킬을 익혀야 합니다.
- DFS, BSF를 구현할 수 있게 되었습니다. 최소한 코드와 다이어그램을 보고 이해할 수 있게 되었습니다.
- 프로그래밍 패러다임은 코드가 정리된 결과라면 리팩토링은 코드를 정리하는 과정을 알려주는 책입니다.

### Lacked

- 하루를 반나절처럼 보내고 있습니다. 하루를 4일처럼 보내야 합니다. 1주일을 1달처럼 6개월을 2년처럼 1년을 4년처럼 보내야 합니다.
- 코테와 면접질문은 모조건 꾸준히 학습해야 합니다.
  - 딜레마는 시간입니다. 시간을 너무 투입하지 않으면 하는 의미가 없습니다. 학습이 별로 없습니다. 시간을 너무 많이 투입하면 개발자로서 코드로 생산한 결과를 기회 비용으로 지불하게 됩니다.

### Longed(잘하기 위해 필요한 것)

- 프로덕트의 MVP를 빠르게 뽑습니다.
- 이력서를 보완합니다.
  - 담당한 역할은 디자인, 프론트엔드, 백엔드 모두 담당했다고 합니다.
- 이력서 보완을 위해서 프로덕트 MVP를 뽑는 과정을 블로그로 정리합니다.
- 포트폴리오 자료를 따로 만듭니다.
  - Notion으로 MVP를 뽑습니다.
  - Next.js로 마이그레이션 합니다.

### Action Item

- [ ] 프론트엔드 프로덕트 MVP 릴리즈
- [ ] 이력서 리팩토링
  - [ ] 이력서 심미성은 보류하고 순수하게 내용위주로 변경
  - [ ] 비즈니스적으로 문제로 인식한 것부터 역할과 성과 그리고 의사결정 과정 정리(상황-행동-결과)
- [ ] 포트폴리오 페이지 만들기
  - [ ] 상세 달성 성과 나열하기
- [ ] 코테와 면접 질문은 꾸준히 진행하기
  - 면접 질문은 복습 시스템 만들기 시작하기
  - 코테는 기출 문제 위주로 점진적으로 옮기기
  - 자료구조 알고리즘은 다른 복습 자료 활용하고 추가하기

## [MSW] Warning: captured a request without a matching request handler:

> [MSW] Warning: captured a request without a matching request handler:

MSW를 사용하는데 이런 경고 메시지를 받았습니다.

일단 해결은 상당히 단순했습니다.

```tsx
if (process.env.NODE_ENV === 'development') {
  worker.start({ onUnhandledRequest: 'bypass' });
}
```

[MSW logging warnings for unhandled Supertest requests](https://stackoverflow.com/questions/68024935/msw-logging-warnings-for-unhandled-supertest-requests)

그래서 일단 Stack overflow에서 검색하고 해결책을 바로 적용했습니다.

하지만 의문이 있습니다. 그래서 일단 chatGPT에 질문했습니다.

> [MSW] Warning: captured a request without a matching request handler:
>
> 이런 경고 메시지를 받았습니다.
>
> 일치하는 해더 없이 요청을 포착했다고 의미하는가?
>
> 만약 일치하는 해더 없이 요청을 포착했다면 MSW로 mocking하는데 무슨 문제가 있는 것인가? 아니면 무슨 문제가 생길 수 있는가?

> "MSW"는 Mock Service Worker의 약어로, 개발 및 테스트 목적으로 실제 서버 요청을 가로채고 가짜 응답을 제공하는 도구입니다. 경고 메시지 "Warning: captured a request without a matching request handler"는 MSW에서 발생하는 것으로, 요청을 가로챘지만 해당 요청에 대한 처리기(handler)가 없다는 것을 의미합니다.
>
> 이러한 경고 메시지가 나타나는 이유는 다음과 같습니다:
>
> 1. 요청을 가로채기 위해 등록한 모의(request)와 실제로 수신된 요청이 일치하지 않을 때 발생할 수 있습니다. 예를 들어, 등록한 모의 요청과 메서드, 경로 또는 헤더 등이 일치하지 않는 요청이 발생하면 이 경고가 표시됩니다.
>
> 2. MSW에서 등록한 요청 처리기(handler)가 설정되지 않은 경우에도 이 경고가 나타날 수 있습니다. 요청을 가로챌 때 해당 요청에 대한 처리 방법을 정의하는 요청 처리기가 등록되어 있어야 합니다.
>
> 이러한 문제가 발생할 경우 MSW mocking에 문제가 있는 것입니다. 이는 실제 서버 응답을 제공하는 대신 가짜 응답을 반환하도록 구성되어 있으므로, 등록된 요청 처리기가 없으면 원하는 응답을 제공할 수 없게 됩니다. 따라서 응답을 처리할 수 있는 적절한 요청 처리기를 등록하는 것이 중요합니다.
>
> 문제가 생길 수 있는 가능성은 다음과 같습니다:
>
> 1. 실제 서버와의 통신이 필요한 기능을 모킹하고 있을 때, 해당 요청을 처리하기 위해 등록된 처리기가 없으면 올바른 응답을 받을 수 없게 됩니다.
>
> 2. 요청 처리기가 부적절하게 구성되어 있다면, 가짜 응답이 실제 서버의 동작과 일치하지 않을 수 있습니다. 이는 개발자가 응답을 테스트하거나 디버깅할 때 문제를 일으킬 수 있습니다.
>
> 따라서 MSW를 사용할 때는 등록된 요청 처리기가 요청과 일치하도록 확인하고, 필요한 요청에 대해 적절한 가짜 응답을 제공할 수 있도록 설정해야 합니다.
>
> \- chatGPT

MSW로 서버를 흉내내는데 잘못 흉내내는 문제라고 생각할 수 있습니다. 다양한 대응 방침이 있습니다. 일단 단순하게 기능을 구현하고 통신 동작에 익숙해지면 추가하는 전략이 있습니다.

사족으로 MSW로 조기에 설정할 필요는 없습니다. 프로젝트가 성숙해졌을 때 도입해도 늦지 않을 것 같습니다.

### handler 관심사 분리

handler 관심사 분리는 중요합니다. 저는 개인프로젝트이지만 현업에서 mocking할 백엔드 코드의 숫자는 엄청나게 많습니다. 그래서 관심사를 분리하는 것이 중요합니다.

```ts
// handlers/index.ts
import type { DefaultBodyType, MockedRequest, RestHandler } from 'msw';
import * as cardHandlers from './cardHandlers';
import * as authHandlers from './authHandlers';

export const handlers: RestHandler<MockedRequest<DefaultBodyType>>[] = [
  ...Object.values(cardHandlers),
  ...Object.values(authHandlers),
];
```

여기서도 인덱스 엔트리를 잘 활용하는 것이 중요합니다.

[MSW로 API 모킹하기](https://blog.mathpresso.com/msw%EB%A1%9C-api-%EB%AA%A8%ED%82%B9%ED%95%98%EA%B8%B0-2d8a803c3d5c)

위 아티클을 보고 따라했습니다.

## 인덱스 엔트리

```tsx
// component/Navbar/index.tsx
function Navbar() {
  return <nav>home</nav>;
}

export { Navbar };
```

```tsx
// component/index.ts
export * from './Navbar';
```

```tsx
// Layout.tsx
import { Global } from '@emotion/react';
import GlobalStyle from '../styles/Reset';
import { Navbar } from '../Components';

function Layout({ children }: { children: React.ReactNode }) {
  return (
    <>
      <Global styles={GlobalStyle} />
      <Navbar />
      {children}
    </>
  );
}

export default Layout;
```

기존보다 index 엔트리를 더 간결하게 작성하는 방법을 적용했습니다.

## 스타일링 관심사 분리

`Styled`에서 접근하지 말고 바로 컴포넌트명 그래도 활용하는 것이 좋겠습니다. 가독성을 너무 저해합니다. 또 인덱스 엔트리 배웠다고 바로 활용하는데 꼭 좋은 것 같지는 않습니다.

스타일링과 관련된 코드를 다른 모듈로 분리해서 마크업 정보를 담는 관심사와 스타일링을 담는 관심사를 분리하는 것은 좋습니다.

의도는 좋은데 막상 해보니까 가독성이 너무 없습니다. 모든 것을 인덱스 엔트리로 처리할 필요는 없습니다.

```tsx
// /Components/Navbar/index.ts
import * as Styled from './Navbar.style';

function Navbar() {
  return (
    <Styled.Navbar>
      <Styled.Container>
        <Styled.LeftList>
          <Styled.ListItem>home</Styled.ListItem>
          <Styled.ListItem>Deck</Styled.ListItem>
        </Styled.LeftList>
        <Styled.RightList>
          <Styled.ListItem>Setting</Styled.ListItem>
        </Styled.RightList>
      </Styled.Container>
    </Styled.Navbar>
  );
}

export { Navbar };
```

```tsx
// /Components/Navbar/Navbar.style.tsx
import styled from '@emotion/styled';

export const Navbar = styled.nav`
  height: 4rem;
  width: 100%;
  background-color: #f8f8f8;
  display: flex;
  align-items: center;
  padding: 0 2rem;
`;

export const Container = styled.div`
  display: flex;
  justify-content: space-between;
  width: 100%;
`;

export const LeftList = styled.ul`
  display: flex;
`;

export const RightList = styled.ul``;

export const ListItem = styled.li``;
```

Styled를 접두어를 붙이는 코드를 봤습니다. 가독성을 해칩니다.

일단 익숙한 JSX 문법으로 스타일을 작성하고 활용한다는 점은 좋습니다.

https://github.com/wanted-frontedend-team5/pre-onboarding-10th-2-5/tree/main/src/components/SearchBar

## RRD 라우팅

너무 오래간만에 해서 조금 당황스럽습니다.

Link 태그 사용하면 해결되는 문제였습니다.

```tsx
import { Link } from 'react-router-dom';

function Navbar() {
  return <Link to={'/cards'}>Home</Link>;
}

export { Navbar };
```

생각보다 단순하게 해결할 수 있었습니다.

## 조건부 랜더링 관심사 분리

```tsx
import { Link } from 'react-router-dom';
import { Nav, Container, List, ListItem } from './Navbar.style';
import { useLogin } from '../../hooks';

function Navbar() {
  const { isLoggedIn } = useLogin();

  return (
    <Nav>
      <Container>
        {isLoggedIn ? (
          <>
            <List>
              <ListItem>
                <Link to={'/cards'}>Home</Link>
              </ListItem>
              <ListItem>
                <Link to={'/deck'}>Deck</Link>
              </ListItem>
            </List>
            <List>
              <ListItem>
                <Link to={'/setting'}>Setting</Link>
              </ListItem>
            </List>
          </>
        ) : (
          <>
            <List>
              <ListItem>
                <Link to={'/'}>Home</Link>
              </ListItem>
            </List>
            <List>
              <ListItem>
                <Link to={'/signup'}>Sign Up</Link>
                <Link to={'/signin'}>Sign In</Link>
              </ListItem>
            </List>
          </>
        )}
      </Container>
    </Nav>
  );
}

export { Navbar };
```

이런 코드가 있습니다. 여기서 고민은 조건부 랜더링이 나오면 바로 리팩토링 대상이라고 했습니다. 여기서 고민입니다.

- 다른 모듈에 담고 호출하는 것이 적절할까?
- 하위에 export 안하고 배치할까?

- `function` 키워드의 장점을 활용하면 호이스팅 현상이 이점으로 작용할 수 있습니다. 제일 중요하고 외부에서 접근할 수 있는 함수를 최상단에 배치할 수 있습니다. 그리고 조건부 랜더링을 위해 있어야 할 함수는 하위에 유지할 수 있습니다. 즉 다른 모듈로 분리하지 않고 바로 관심사를 분리할 수 있습니다.
- 여기서 더 고민해볼 수 있습니다. 다른 모듈로 분리해야 하는 이유는 무엇인가? 관심사의 분리가 이유인데 관심사는 마크업으로 정보를 어떤 관계로 어떻게 보여주는가? 이것이 관심사입니다. 그리고 마크업 내에서 주입받아야 할 로직이 없습니다. 다른 모듈로 분리했을 때 가독성을 저해할 것 같지 않습니다.

```tsx
import { Link } from 'react-router-dom';
import { Nav, Container, List, ListItem } from './Navbar.style';
import { useLogin } from '../../hooks';

export function Navbar() {
  const { isLoggedIn } = useLogin();
  return <Nav>{isLoggedIn ? <LoggedInNav /> : <LoggedOutNav />}</Nav>;
}

function LoggedInNav() {
  return (
    <Container>
      <List>
        <ListItem>
          <Link to={'/cards'}>Home</Link>
        </ListItem>
        <ListItem>
          <Link to={'/deck'}>Deck</Link>
        </ListItem>
      </List>
      <List>
        <ListItem>
          <Link to={'/setting'}>Setting</Link>
        </ListItem>
      </List>
    </Container>
  );
}

function LoggedOutNav() {
  return (
    <Container>
      <List>
        <ListItem>
          <Link to={'/'}>Home</Link>
        </ListItem>
      </List>
      <List>
        <ListItem>
          <Link to={'/signup'}>Sign Up</Link>
        </ListItem>
        <ListItem>
          <Link to={'/signin'}>Sign In</Link>
        </ListItem>
      </List>
    </Container>
  );
}
```

- 일단 관심사를 분리하는 것은 올바른 선택은 맞았습니다. `fragment`에 의존하지 않게 되었습니다.

- 순수하게 마크업만 담당하고 로직을 주입받지 않기 때문에 같은 모듈 내에 유지해도 괜찮을 것 같습니다. 로직을 주입받아야 하는 시점에 다른 모듈로 분리해도 늦을 것 같지 않습니다.

## Nav 컴포넌트의 테스트 가능성

> Cannot destructure property 'basename' of 'React\_\_namespace.useContext(...)' as it is null.

```
Components/Navbar/index.tsx
```

Nav는 `Layout` 컴포넌트에 넣고 사용하고 있습니다. 문제는 테스트할 때 발생했습니다.

```tsx
import { Global } from '@emotion/react';
import GlobalStyle from '../styles/Reset';
import { Navbar } from '../Components';

/**
 * @see https://github.com/WANTED-TEAM03/pre-onboarding-10th-1-3/blob/main/src/routes/_globalLayout.tsx
 */
function Layout({ children }: { children: React.ReactNode }) {
  return (
    <>
      <Global styles={GlobalStyle} />
      <Navbar />
      {children}
    </>
  );
}

export default Layout;
```

Nav가 정상동작하기 위해서는 개별 페이지별로 호출하는 방식으로 사용해야 한다는 것입니다.

```tsx
import { BrowserRouter, Route, Routes } from 'react-router-dom';
import Layout from './GlobalLayout';
import {
  Cards,
  Deck,
  Landing,
  NotFound,
  Setting,
  SignIn,
  SignUp,
} from '../pages';

function Router() {
  return (
    <BrowserRouter>
      <Layout>
        <Routes>
          <Route path="/" element={<Landing />} />
          <Route path="/cards" element={<Cards />} />
          <Route path="/deck" element={<Deck />} />
          <Route path="/setting" element={<Setting />} />
          <Route path="/signin" element={<SignIn />} />
          <Route path="/signup" element={<SignUp />} />
          <Route path="*" element={<NotFound />} />
        </Routes>
      </Layout>
    </BrowserRouter>
  );
}

export default Router;
```

이렇게 컨텍스트 밖에 있는 것이 문제로 작용했습니다.

여기서 고민할 점은 당장해결할지 아니면 후순위로 두고 다른 가치가 더 높은 것에 대응할지입니다.

지금 시점에서는 기능 구현이 우선순위에서 높습니다. 따라서 추가 테스트 코드 작성 중에 혹은 리팩토링 진행 직전에 테스트를 추가합니다.
