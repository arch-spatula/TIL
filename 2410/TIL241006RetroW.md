# 잠시 자유 프로젝트 10일차

1일1커밋 무사고: 664일차

## 감사일기

1. ???

- [x] 주간회고
- [x] 주간줍줍
- [ ] 다시한 번 dotfile 할 수 있을까?
  - [ ] brew에서 nix-darwin으로 마이그레이션
  - [ ] neovim 재설정
- [ ] LSP란 어떻게 동작하는가?
  - [x] 시도
  - [ ] lua를 위한 neovim 설정
- [ ] nuxt 마이그레이션 글 탈고 및 편집
  - [ ] 기존 아이디어, 초고 단계의 글들 분석하고 계획하기
  - [ ] 배포 단계 정리하기
- [ ] TIL-CLI 1.0.1
  - [ ] JSON 파일 다시 설정
  - [ ] 입력 설계
  - [ ] 테스트 설계
  - [ ] 입력 - 처리 - 출력 MVC 패턴 구축
  - [ ] 실행파일 별칭 지정
- [ ] 회사 관련된 소프트스킬들 정리하기
  - [x] 정산 절차
  - [ ] 질문 및 커뮤니케이션
  - [ ] 디버깅 전략
  - [ ] 성능 최적화
  - [ ] 소스코드 보기
- [ ] NEOVIM 회사에서 사용가능하게 만들기
  - [ ] 백엔드 때문에 C# 언어 설정
  - [ ] 회사에서 읽을 도서를 위해 JAVA 언어 설정
- [ ] GO 언어 블랙잭
- [ ] 플래시 카드 2.0 서비스 만들기
  - [ ] NUXT 설치
  - [ ] MONGOOSE ORM 설치
  - [ ] VERCEL 배포
  - [ ] 로그인 구현
  - [ ] 어드민 전용기능(배치 삭제, 생성 제한)
  - [ ] 핀터레스트 레이아웃 구현
  - [ ] 문제 유형 태그 구현
  - [ ] 카나리 설정

---

## 주간 회고

### Liked

- nvchad로 잠시 neovim을 바꾸고 golang을 설정했는데 적당한 것 같습니다.
  - 이전 neovim에 사용하던 ascii art도 nvchad 컨샙에 맞게 가져와 상당히 만족스럽습니다.
- 이번주에 블로그를 nuxt content로 다시 만들고 배포했습니다. 
  - 이제는 개발 과정만 글로 정리해서 올리면 됩니다.

### Learned

- nvchad를 사용하면서 가장 강력한 기능은 키바인딩 검색 toggle(`leader` + `c` + `h`)이라고 봅니다.
- 피드백은 가능하면 빠르고 일찍 받는게 유리한 것 같습니다. 작업이 되었고 다른 사람을 의존하고 있는 부분이 있으면 피드백을 얻어내야 합니다. 다른 작업 때문에 언제 착수가능한지 알아내야 합니다. 적당한 시점에 적당한 재촉을 해야 상대도 어느정도 여유를 갖거나 조기에 시간관리 문제를 대응할 수 있습니다.

### Lacked

- 제가 직접 설정한 neovim 하자 때문에 더이상 LSP 실습 진행에 문제가 될 것이라고 착각했습니다.
  - 실제로 문제가 되는 부분은 다른 것이었습니다.
  - 메서드에 잘못된 값을 반환하고 있었습니다.
  - 끝까지 보기 위한 끈기가 부족했던 것 같습니다. 개인적으로 LSP를 탐구하기 위해 시도한 프로젝트인데 일찍 중단하게 되었습니다.

### Longed(잘하기 위해 필요한 것)

- 잠시 nvchad를 사용하면서 nvchad의 철학에 익숙해져야 합니다.
- 끈기를 다시 생각해야 합니다. 문제가 무엇인지 아직도 이해를 잘 못하면 이해를 시도하지 않고 바로 그만두었습니다. 이것을 극복해야 합니다.
- 지난주 목표랑 같습니다. 문제를 해결하지 않고 있습니다.
  - 문제를 단순화하고 문제를 해결해야 합니다. 한번에 몇가지 문제만 해결해야 합니다.
- 개발과 관련된 콘텐츠를 봐도 개발에 의견에 대한 콘텐츠만 많습니다. 실제 개발의 내부 동작에 관한 것은 별로 없습니다. 개발을 이해하기 위한 콘텐츠를 늘려야 합니다. 

### Action Item

- [ ] LSP란 어떻게 동작하는가?
  - [ ] ???
- [ ] nuxt 마이그레이션 글 탈고 및 편집
  - [ ] 기존 아이디어, 초고 단계의 글들 분석하고 계획하기
  - [ ] 배포 단계 정리하기

---

```lua
local client = vim.lsp.start_client({
	name = "educationalsp",
	cmd = { "실행파일 위치" },
    -- 아래는 개인적인 설정
	-- on_attach = require("plugins.lsp").on_attach,
})

if not client then
	vim.notify("hey, you didnt do the client thing good")
	return
end

vim.api.nvim_create_autocmd("FileType", {
	pattern = "markdown",
	callback = function()
		vim.lsp.buf_acttach_client(0, client)
	end,
})
``` 
