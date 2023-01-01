# 감사일기

1. ???
2. ???
3. ???

00:00

# todo

- [x] 학원 수업 참석
- [x] 리액트 Hook 별 자료 정리 시작

# 월간 회고

- 바닐라 자바스크립트로 ToDoList App CRUD를 할 수 있게 되었습니다.
- React로 간단한 ToDoList App을 만들 수 있게 되었습니다. 훅 useState, useEffect 2개를 사용할 줄 알게 되었습니다.
- 함수형 자바스크립트 프로그래밍을 체험해보게 되었습니다.
  - 하지만 단순한 체험이었습니다. Jest까지 같이 사용하려고 했지만 마찬가지로 체험만 남았습니다.
- 코어 자바스크립트 책을 완독했습니다. 개념이 부족해서 2달 뒤에 다시 읽고 한 번에 이해해야 합니다.
- Freecodecamp React 2022 12시간 강의를 완강했습니다. 리액트를 입문하게 되었습니다.
- 인터넷 강의를 수강하려고 했지만 계속 뒤로 미루었습니다. 기초 부분은 뒤로하고 모르는 부분부터 배워야 합니다. 하지만 기초부터 하면서 비효율적이라고 느끼고 있습니다.

## Liked

- 상당히 많은 목표를 이루었습니다.

## Learned

- 결국 React를 배우고 입문했습니다.
- 자바스크립트도 이해하는데 깊이가 생겼습니다.
- todoApp도 만들었습니다.

## Lacked

- React만 입문하고 다른 프레임워크도 적어도 입문은 해야 하는데 미루었습니다.

## Longed(원하는 것)

- 지난 2주동안 MERN stack 전반을 이해하고 싶었습니다.

## Action Item

- [ ] 남는 시간에 생활코딩 Express부터 시작합니다.
- [ ] 유데미 인강을 수강합니다.

# Git 특강

- 깃이 없다면 소스코드 변경 히스토리를 파악하기 어렵습니다.
  - 소스코드 관리비용이 커집니다.
  - 변경하고 보안취약, 버그, 나쁜 사용성을 이유로 과거 버전으로 돌아기 어렵습니다.
- 깃이 없다면 협업 비용이 커집니다.
  - 소스코드가 만줄은 금방 넘어갑니다.
- 깃을 만든 사람은 리눅스 운영체제를 만든사람입니다. git은 오픈소스입니다. 그래서 모든 개발자들이 만들 수 있습니다.
- 깃은 버전을 관리하는 툴입니다. 개발에서 버전은 흔합니다. 버전은 변경사항입니다. 버전은 유의미한 변화가 결과물로 나올 때를 기준으로 합니다. 유의미한 작은 변화를 쌓아나가는 과정입니다.
- 깃허브는 원격 저장소 호스팅 서비스입니다. 저장소는 깃으로 관리하는 프로젝트입니다. 저장소에 저장하는 것은 코드베이스 입니다. 호스트는 관리입니다.
- 소스 트리를 사용할 없는 경우에서는 `git` 커맨드를 사용할 수 있어야 합니다. 일상에서는 소스트리를 활용하지만 필요하면 커맨드도 활용합니다.
- 작업 디랙토리(워킹트리), 스테이지(인덱스), 저장소가 있습니다. 스테이지와 저장소는 가상공간입니다.
  - 버전을 만들위해서는 변경이 있어야 합니다.
  - 디랙토리는 컴퓨터 실제 공간입니다. `.git`이 디랙토리에 있습니다.
  - 스테이지는 다음 버전에 올라갈 후보들이 있을 공간입니다.
    - 모든 것을 스테이징할 필요는 없습니다.
  - 저장소는 영어로 리포지토리라고 합니다.

```zsh
git init
```

Initialized empty Git repository 이런 문구가 나옵니다. 저장소 생성했다는 피드백입니다.

```shell
ls -a
```

숨김폴더까지 보여달라는 명령입니다.

```shell
ls -al
```

숨김 폴더에 대한 정보를 더 자세히 보여줍니다.

`git add`는 `Create`, `Update`, `Doc` 처럼 변경사항을 따로 올리고 `commit`합니다. 그렇게 해서 `push`하고 `merge`합니다.

```shell
git rm --cached (파일이름)
```

실수로 `add`로 올리면 내리는 방법입니다.

```zsh
git config --global user.email "(여러분이메일)"
git config --global user.name "(여러분이름)"
```

새 컴퓨터 사면 이 설정 까먹지 마세요. `git config --global user.email`, `git config --global user.name`만 처서 개인정보를 확인하도록 합니다.
커밋해시는 각각의 버전에 대한 고유한 문자열입니다.

tegongkang@gmail.com 여기에 학생 아이디 보냅니다.

원격 저장소는 서버에 저장합니다. github에 백업할 수 있습니다.

https://github.com/arch-spatula/learningGitAndGithub

URL은 직관적으로 `github.com` 도메인 `arch-spatula` 유저 도메인 `learningGitAndGithub` 저장소로 나누어 저있습니다.

원격 저장소 4가지 상호작용 clone, pull, push, fetch

`clone`: 원격 저장소를 로컬 저장소에 복제하는 명령
`push`: 로컬 저장소에서 원격 저장소에 반영시키는 명령
`pull`: 업데이트 된 원격 저장소를 로컬에 반영하는 명령

git 삭제

```shell
git -D (branch 이름)
```

# 브랜칭 실수

dev 같은 브랜치는 github 웹에서 만들고 브랜치를 clone합니다.

# Fetch Post

https://stackoverflow.com/questions/6396101/pure-javascript-send-post-data-without-a-form

https://developer.mozilla.org/en-US/docs/Web/API/fetch
