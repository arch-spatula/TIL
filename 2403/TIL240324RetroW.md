# neovim-setup 0.2.0 3일차

1일1커밋 무사고: 468일차

## 감사일기

1. 아이폰으로 바꾼 것에 감사합니다. 옛날 폰 보안 취약점을 덜 걱정하면서 살수 있게 되었습니다.

- [x] 주간회고
- neovim
  - [x] vue 하이라이트 및 LSP 지원
    - [x] sub 브랜치 추가
    - [x] sub 브랜치에서 환경변수 설정 시도 및 vue LSP 연결 시도
    - [x] 환경변수 호출하는 방법 정리하기
- [ ] 블랙잭 만들기
- 와이어 시스템
  - [x] 텍스트 버튼
  - [ ] 컬러 문서
    - [ ] css 변수(50 ~ 600)
    - [ ] 상수 문자열
  - [ ] 아이콘 문서
    - [ ] 문서 만들기
  - [ ] 아코디언
  - [ ] 스낵바 or 토스트 메시지
  - [ ] input 이중 ref
- 문해력
  - [ ] 문제 7장 풀기
    - [ ] 6
    - [x] 7
- 개발자 블로그
  - [ ] 호스팅 플랫폼
    - [ ] Attack Challenge Mode
      - [ ] 문서 읽고 요약 정리
    - [ ] Deployment Protection on Vercel
      - [ ] 문서 읽고 요약 정리
    - [ ] DDoS Mitigation
      - [ ] 문서 읽고 요약 정리
    - [ ] DDoS란 무엇인가?
    - [ ] 방화벽이란 무엇인가?
      - [ ] 대표적인 보안 규칙은 무엇인가?
      - [ ] DMZ란 무엇인가?
      - [ ] 스위치 및 라우터 등 어떤 네트워크 장비를 사용하는가?
      - [ ] C 언어로 구현은 어떻게 할 수 있는가?
    - [ ] 방어 전략이란 무엇인가?
  - [ ] C 언어 숫자 야구 CLI DIY-CS에 추가
    - [ ] 버퍼를 수동으로 비우도록 설계한 이유는 무엇인가?
      - [x] 자료 찾기
      - [ ] 자료를 이미지와 함께 자세하게 정리하기
      - [ ] 버퍼 메모리란 무엇인가?
      - [ ] `scanf`의 동작 원리는 무엇인가?
    - [ ] `fgets`란 무엇인가?
      - [ ] 자료 찾기
      - [ ] 함수의 목적은 무엇인가?
      - [ ] 스트림이란 무엇인가?

---

## 주간 회고

- 문해력
  - [ ] 문제 7장 풀기
    - [x] 1
    - [x] 2
    - [x] 3
    - [x] 4
    - [x] 5
    - [ ] 6
    - [x] 7
- neovim
  - [x] Mason에서 LSP이외 것 확정 설치하는 방법
  - [x] git 커밋 준비를 위한 플러그인
  - [x] github PR 및 이슈 템플릿
  - [x] vue 하이라이트 및 LSP 지원
  - [x] Noice
- [ ] 블랙잭 만들기
- 와이어 시스템
  - [x] 텍스트 버튼
  - [ ] 컬러 문서
    - [ ] css 변수
    - [ ] 상수 문자열
  - [ ] 아이콘 문서
    - [ ] 문서 만들기
  - [ ] 아코디언
  - [ ] 스낵바 or 토스트 메시지
  - [ ] input 이중 ref
- 개발자 블로그
  - [ ] 호스팅 플랫폼
  - [ ] C 언어 숫자 야구 CLI DIY-CS에 추가

### Liked

- neovim에서 골머리였던 확정 설치 방법과 vue LSP 디렉토리를 환경변수로 받아 오는 방법을 찾아냈습니다.
- 부족한 문해력을 극복하게 위해 작게 실천하는 활동을 비교적 꾸준하게 실천했습니다.

### Learned

- 프론트엔드 엔지니어는 브라우저 지식도 풍부해야 하지만 또 컴퓨터 그래픽 지식도 풍부해야 합니다. 저는 컴퓨터 그래픽 지식이 없었습니다. 컴퓨터 공학 분야로 생각하지 않고 등한시 했습니다.
- 터치타이핑도 못하는데 vim을 사용하면 오히려 독이된다고 합니다. 당장 극복해야 합니다.
- 지금 주된 프로젝트 선정을 잘못했습니다. 지금 집중하는 것은 디자인 시스템을 만다는 것이 아니고 neovim 과 관련된 설정에 집중하고 있었습니다.

### Lacked

- 이번주에는 neovim 설정만 주구장창 했습니다.
- 회사에서는 디버깅을 많이 했습니다. 간과했던 부분 중 하나는 API 소비자로서 http 밴치마크도 문제를 이야기 해야 합니다. 데이터 사이즈가 커지면 처리시간이길어집니다. 이 길어진 시간을 문제라고 이야기해야 합니다.
- 작업이 완료되면 상태를 명시해야 합니다. 이것을 자꾸 잊습니다.

### Longed(잘하기 위해 필요한 것)

- 작업의 상태 관리는 다른 작업에 착수하는 시간이 늘려져도 그냥 보면서 바꿉시다.
- 문해력이라는 근본적인 문제를 해결하기 전에 정보처리기사를 먼저 해결해야 합니다. 문해력은 끝이나는 순간 정보처리기사 문제를 풀기 시작할 것입니다.
- 블로그 관리를 위해 글을 써야 하는데 아직도 진전이 너무 없습니다.
- 디자인 시스템 0.1.0을 빠르게 마무리하고 블로그 정리를 끝내고 다음 목표를 설정해야 합니다. 정보처리기사를 위해 공부할지 C 언어 도서를 읽을지 결정해야 합니다.

### Action Item

- [ ] 블랙잭 만들기
- 와이어 시스템
  - [ ] 컬러 문서
    - [ ] css 변수(50 ~ 600)
    - [ ] 상수 문자열
  - [ ] 아이콘 문서
    - [ ] 문서 만들기
  - [ ] 아코디언
  - [ ] 스낵바 or 토스트 메시지
  - [ ] input 이중 ref
- 문해력
  - [ ] 문제 7장 풀기
    - [ ] 1
    - [ ] 2
    - [ ] 3
    - [ ] 4
    - [ ] 5
    - [ ] 6
    - [ ] 7
- 개발자 블로그
  - [ ] 호스팅 플랫폼
    - [ ] Attack Challenge Mode
      - [ ] 문서 읽고 요약 정리
    - [ ] Deployment Protection on Vercel
      - [ ] 문서 읽고 요약 정리
    - [ ] DDoS Mitigation
      - [ ] 문서 읽고 요약 정리
    - [ ] DDoS란 무엇인가?
    - [ ] 방화벽이란 무엇인가?
      - [ ] 대표적인 보안 규칙은 무엇인가?
      - [ ] DMZ란 무엇인가?
      - [ ] 스위치 및 라우터 등 어떤 네트워크 장비를 사용하는가?
      - [ ] C 언어로 구현은 어떻게 할 수 있는가?
    - [ ] 방어 전략이란 무엇인가?
  - [ ] C 언어 숫자 야구 CLI DIY-CS에 추가
    - [ ] 버퍼를 수동으로 비우도록 설계한 이유는 무엇인가?
      - [ ] 자료를 이미지와 함께 자세하게 정리하기
      - [ ] 버퍼 메모리란 무엇인가?
      - [ ] `scanf`의 동작 원리는 무엇인가?
    - [ ] `fgets`란 무엇인가?
      - [ ] 자료 찾기
      - [ ] 함수의 목적은 무엇인가?
      - [ ] 스트림이란 무엇인가?

---

[Find and replace strings in vim on multiple lines](https://stackoverflow.com/questions/19994922/find-and-replace-strings-in-vim-on-multiple-lines)

## 선입견을 가져라

https://www.youtube.com/watch?v=Q5EuiZkzOH0

- 단순하게 원칙만으로 보면 나쁜 것으로 보입니다.
  - 어떤 대상에 대하여 이미 마음속에 가지고 있는 고정적인 관념이나 관점.
- 본인이 간접적인 경험으로 어떤 생각이 굳어집니다. 반대 견해를 봐도 바뀔 수 있어야 합니다. 과거의 경험을 기억하고 활용하는데 같은 실수를 반복하는 문제가 있습니다.
- 주장도 선입견으로 생각되면 선입견을 갖고 있어야 합니다.
- 경험은 자산이고 활용해야 하는데 선입견을 갖지말라고 하는데 아닙니다.
- 과거에 성능, 버그, 코드 퀄리티 등 문제를 만들던 사람의 유형을 한번 봤으면 다음에 면접을 보러 들어가면 과감하게 탈락시킬 수 있어야 합니다.
- 틀리기 싫어서 판단을 안 하는 것도 결국에는 틀린 것입니다. 차라리 판단을 틀리고 귀납적 결론을 수정하도록 합니다.
- 통계도 일종의 선입견입니다. 통계학으로 분석하고 의사결정을 하는데 의사결정을 위해 견해를 만들 때 선입견입니다. 나쁘다는 것이 아닙니다.

## 환경변수 호출하는 방법 정리하기

제일 도움되는 자료는 이 질문이었습니다.

[Use variable from external file in Neovim init.vim](https://stackoverflow.com/questions/74087692/use-variable-from-external-file-in-neovim-init-vim)

저랑 겪은 비즈니스 컨텍스트 문제가 동일합니다.

저는 맥북에서 사용한 디렉토리랑 회사에서 사용하는 컴퓨터 디렉토리랑 다릅니다. 이 다른 디렉토리마다 각각 커밋하게 만들고 싶지 않았습니다.

```lua
os.getenv("HOME")
```

위처럼 세션에서 기본적으로 설정된 환경변수를 접근하면 되는 것이었습니다.

처음에는 `require`로 다른 곳에 디렉토리를 하드코딩하고 호출하면 해결될 줄 알았습니다. 전혀 해결이 안되었습니다. 오히려 해당하는 디렉토리를 전혀 못찾았습니다.

그래서 환경 변수를 설정하기로 했습니다. 환경변수를 설정하겠다고 했는데 문제가 있습니다. 도대체 무슨 환경변수인가? 나약한 현대 웹개발자인 저에게 환경변수는 `.env` 파일에 키와 값으로 쓰는 것을 생각했습니다. 하지만 neovim과 lua 세계에서 달랐습니다. shell RC(zshell, bash, posh ...)에 설정한 에일리어스를 의미하는 것이었습니다.

본인이 설정한 쉘 파일이 있다면 각자 접근하기 바랍니다. 저는 omz에 `.zshrc`로 설정했습니다.

```sh
nvim .zshrc
```

여기서 본인이 설정한 에일리어스를 확인해보기 바랍니다. 기본적으로 맥은 zsh로 설정되어있습니다.

윈도우는 [자습서 - Oh My Posh를 사용하여 PowerShell 또는 WSL에 대한 사용자 지정 프롬프트 설정](https://learn.microsoft.com/ko-kr/windows/terminal/tutorials/custom-prompt-setup)을 참고하기 바랍니다.

```sh title=".zshrc"
# 파일명 .zshrc
# HOME은 이미 기본설정되어 있음
export MYVIMRC="Foo"
```

약간 주의할 점들이 있습니다.

1. `export` 키워드가 없으면 환경변수로 접근할 수 없습니다.
2. 환경변수의 키(지금 예시는 `MYVIMRC`입니다.)는 모두 대문자로 표기해야 합니다. 상수라 적절하기는 합니다.
3. shell RC 파일의 설정이 적용되도록 실행하는 과정(지금의 경우 `source ~/.zshrc`)을 잊지 마세요.
4. 터미널을 한번 껐다가 켜보세요.

팁을 드리자면 현재 설정되어 있는지 확인해볼 수 있는 명령이 있습니다.

[Get value of $MYVIMRC from Lua](https://vi.stackexchange.com/questions/31737/get-value-of-myvimrc-from-lua)

```sh
:lua print(os.getenv("MYVIMRC"))
```

위처럼 하면 neovim 내에서 값을 확인해볼 수 있습니다. lua를 REPL으로 이런저런 작업을 해볼 수 있습니다.

참고로 `$`을 조심하세요.

[quick question: os.getenv() works for "PATH" but not "LUA_PATH"](https://www.reddit.com/r/lua/comments/xpr0hs/quick_question_osgetenv_works_for_path_but_not/)

```sh
:lua print(os.getenv("$MYVIMRC"))
```

위 명령도 동작합니다. 실제 값을 활용하고 접근하고자 할 때 `$`을 제거하도록 합니다. `os.getenv("$MYVIMRC")`이렇게 작성하면 `nil`을 반환할 가능성이 높습니다.

```lua title="lsp.lua"
local secret = os.getenv("VUELSPPATH")
if secret == nil then
    print("Environment variable PATH not set")
else
    lspconfig.tsserver.setup({
        init_options = {
            plugins = {
                {
                    name = "@vue/typescript-plugin",
                    location = secret,
                    languages = {
                        "typescript",
                        "javascript",
                        "vue",
                    },
                },
            },
        },
        filetypes = {
            "javascript",
            "typescript",
            "vue",
        },
        capabilities = capabilities,
    })
end
```

저는 VUE LSP를 로컬에 설치해야 동작할 수 있었습니다. 그래서 환경변수로 이렇게 설정하고자 했습니다.

지금 관점에서 다시 보면 코드의 다양한 문제가 있습니다. 상수라고 작성했지만 언어스코어로 띄어쓰기를 표시할 수 있어야 합니다.

nest.js처럼 타입스크립트를 작성해야 하는 경우가 있는데 vue LSP 접근에 실패한 것에 대해서 영향을 받는다는 점이 부조리해 보입니다.

```lua
local secret = os.getenv("VUELSPPATH")
if secret == nil then
    print("VUE LSP PATH not set")
    lspconfig.tsserver.setup({
       capabilities = capabilities,
    })
else
    lspconfig.tsserver.setup({
        init_options = {
            plugins = {
                {
                    name = "@vue/typescript-plugin",
                    location = secret,
                    languages = {
                        "typescript",
                        "javascript",
                        "vue",
                    },
                },
            },
        },
        filetypes = {
            "javascript",
            "typescript",
            "vue",
        },
        capabilities = capabilities,
    })
end
```

이게 더 적절해 보입니다. 여기서 의문은 환경변수를 조건부로 접근하고 싶습니다. 버퍼가 vue가 아닌데 vue lsp를 접근하는 환경변수를 읽는 함수를 호출합니다.

이상적인 것은 vue 버퍼에 해당하는지 확인하고 vue lsp가 있는 환경변수를 호출하게 만드는 것입니다.
