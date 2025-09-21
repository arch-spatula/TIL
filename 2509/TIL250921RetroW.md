# 블로그 다시 만들기 83일차

1일1커밋 무사고: 1014일차

## 감사일기

1. ???

- [x] 주간회고
- [ ] 운동
  - [ ] 헬스
    - 클라이밍 다음날 마무리 운동 개념으로 내일 할 계획
  - [ ] 자전거
- [ ] Do it C++ 코딩 테스트
  - [ ] C++ nvim DAP에 표준입력이 가능하게 설정해보기
  - [ ] 2일차
    - 읽다가 사이드 퀘스트가 생겼습니다.
- [ ] 마이크로 튜토리얼
  - [ ] Chapter 4 - Request Lines
  - [ ] Chapter 5 - HTTP Headers
  - [ ] Chapter 6 - HTTP Body
  - [ ] Chapter 7 - HTTP Responses
  - [ ] Chapter 8 - Chunked Encoding
  - [ ] Chapter 9 - Binary Data
- [ ] 블로그 다시 만들기 전 실험
  - [ ] vite로 github pages가 정적 리소스 응답하는 방식 흉내내기
  - [ ] ToC
    - [ ] `data.json`에 h1 ~ h6에 해당하는 데이터 추가
    - [ ] DOM에 붙이기
  - [ ] 검색 팝업에서 tag 클랙해도 input 상태 보존하기
- [ ] 취미로 읽는 통계 관련 자료들
  - [ ] 조사론 필기 옮기기
    - [ ] 6장
    - [ ] 7장
    - [ ] 8장
    - [ ] 9장
    - [ ] 복습

---

## 주간 회고

### Liked

- 마이크로 튜토리얼은 생각을 잘 한 것 같습니다. 아주 오랫동안 해왔어야 하는 것인데 안 했던 것 입니다.

### Learned

- tcp는 극도로 단순합니다. udp도 단순합니다. 물론 프로토콜의 사용자 입장에서 그렇습니다.
- 직장인으로서는 퇴근 후에는 아주 작은 단위로 학습을 해야 효과적입니다. 다른 취미가 있다면 남는 시간이 정말 없습니다.
  - 취미를 포기해야 하는지 아니면 줄이는지 고민을 해야 합니다.

### Lacked

- 이번주는 부지런하게 보낼 줄 알 았는데 전혀 아니었습니다.
- 더 근본적인 문제는 취미가 아니라 절제력과 관련이 있습니다.
  - 더 중요한 일을 더 높은 우선순위로 두고 계속 하겠다는 것이 더 중요합니다.
  - 재미를 위한 운동을 추가하면서 많은 불필요한 시간과 리소스를 사용하고 있습니다.
    - 여가라는 것이 원래 소비활동이 맞지만 과도한 것인지 다시 고민해봐야 할 것 같습니다.
    - 이루고 싶은 것이 많은데 이루고자 하는 것을 실천할 시간이 없다면 결국 못 이룰 것입니다. 시간을 충분히 줘도 어려울 것 입니다.

### Longed(잘하기 위해 필요한 것)

- 마이크로 튜토리얼은 계속 유지해야 합니다.
  - 반드시 동영상의 형태일 필요는 없습니다. 책을 읽고 작은 용어부터 정리하거나 아니면 코테문제를 풀거나 해야 합니다. 항상 무엇을 하는 것이 더 중요한 것 같습니다.

### Action Item

- [ ] 운동
  - [ ] 클라이밍
  - [ ] 헬스
  - [ ] 자전거
- [ ] Do it C++ 코딩 테스트
  - [ ] C++ nvim DAP에 표준입력이 가능하게 설정해보기
  - [ ] 2일차
    - 읽다가 사이드 퀘스트가 생겼습니다.
- [ ] 마이크로 튜토리얼
  - [ ] Chapter 4 - Request Lines
  - [ ] Chapter 5 - HTTP Headers
  - [ ] Chapter 6 - HTTP Body
  - [ ] Chapter 7 - HTTP Responses
  - [ ] Chapter 8 - Chunked Encoding
  - [ ] Chapter 9 - Binary Data
- [ ] 블로그 다시 만들기 전 실험
  - [ ] vite로 github pages가 정적 리소스 응답하는 방식 흉내내기
  - [ ] ToC
    - [ ] `data.json`에 h1 ~ h6에 해당하는 데이터 추가
    - [ ] DOM에 붙이기
  - [ ] 검색 팝업에서 tag 클랙해도 input 상태 보존하기

---

## Chapter 4 - Request Lines

- request line parser를 만들 것인데 이런 것은 본인의 직감으로 한번에 버그 없이 작성할 수 없을 것 같으면 테스트 코드를 넣을 것을 권장합니다.

```
POST /coffee HTTP/1.1
Host: localhost:42069
User-Agent: curl/7.81.0
Accept: */*
Content-Length: 21

{"flavor":"dark mode"}
```

- POST 요청 문자열은 위처럼 작성됩니다. 저 문자열을 파싱해서 다루기 쉬운 형태로 만들 것입니다.

```go
type Request struct {
    RequestLine RequestLine
    Headers     map[string]string
    Body        []byte
}
```

- 위 형태처럼 작성하면 상당히 작관적일 것 같습니다.
  - header는 kv 형태가 될 것이고 body는 json같은 데이터도 많지만 이미지, html, css, js 등 다양합니다.
- `RequestLine`은 첫번째 줄에 대한 표현입니다. 이것은 RFC 명세서가 있습니다. 명세서 기준으로 정확하게 표현할 수 있으면 됩니다.
  - https://datatracker.ietf.org/doc/html/rfc9112#name-message-parsing 여기 있다고 합니다.

```
HTTP-version  = HTTP-name "/" DIGIT "." DIGIT
HTTP-name     = %s"HTTP"
request-line  = method SP request-target SP HTTP-version
```

- SP는 구분을 의미합니다.

```
GET /coffee HTTP/1.1
```

- 위같은 표현을 하면 됩니다.
- 이제 이런 것을 구현할 때는 TDD처럼 테스트를 작성하고 구현하는 것이 적절합니다.
  - 확실한 정답이 있기 때문에 테스트 코드를 작성할 가치가 큽니다.

```go
package request

import (
	"errors"
	"fmt"
	"io"
	"strings"
)

type RequestLine struct {
	Method        string
	RequestTarget string
	HttpVersion   string
}

type Request struct {
	RequestLine RequestLine
	Headers     map[string]string
	Body        []byte
}

var ERROR_MALFORMED_REQUEST_LINE = fmt.Errorf("malformed request-line")
var ERROR_UNSUPPORTED_HTTP_VERSION = fmt.Errorf("unsupported http version")
var SEPARATOR = "\r\n"

func parseRequestLine(b string) (*RequestLine, string, error) {
	idx := strings.Index(b, SEPARATOR)
	if idx == -1 {
		return nil, b, nil
	}

	startLine := b[:idx]
	restOfMsg := b[idx+len(SEPARATOR):]

	parts := strings.Split(startLine, " ")

	if len(parts) != 3 {
		return nil, restOfMsg, ERROR_MALFORMED_REQUEST_LINE
	}

	httpParts := strings.Split(parts[2], "/")
	if len(httpParts) != 2 || httpParts[0] != "HTTP" || httpParts[1] != "1.1" {
		return nil, restOfMsg, ERROR_UNSUPPORTED_HTTP_VERSION
	}

	rl := &RequestLine{
		Method:        parts[0],
		RequestTarget: parts[1],
		HttpVersion:   httpParts[1],
	}

	return rl, restOfMsg, nil
}

func RequestFromReader(reader io.Reader) (*Request, error) {
	data, err := io.ReadAll(reader)
	if err != nil {
		return nil, errors.Join(fmt.Errorf("unable to io.ReadAll"), err)
	}

	str := string(data)
	rl, _, err := parseRequestLine(str)

	if err != nil {
		return nil, err
	}

	return &Request{
		RequestLine: *rl,
	}, nil
}
```

- http 문자열 파서의 일부입니다. 정말 명세서를 읽고 그대로 구현하면 됩니다.

```go
package request

import (
	"strings"
	"testing"

	"github.com/stretchr/testify/assert"
	"github.com/stretchr/testify/require"
)

func TestRequestLineParse(t *testing.T) {
	// Test: Good GET Request line
	r, err := RequestFromReader(strings.NewReader("GET / HTTP/1.1\r\nHost: localhost:42069\r\nUser-Agent: curl/7.81.0\r\nAccept: */*\r\n\r\n"))
	require.NoError(t, err)
	require.NotNil(t, r)
	assert.Equal(t, "GET", r.RequestLine.Method)
	assert.Equal(t, "/", r.RequestLine.RequestTarget)
	assert.Equal(t, "1.1", r.RequestLine.HttpVersion)

	// Test: Good GET Request line with path
	r, err = RequestFromReader(strings.NewReader("GET /coffee HTTP/1.1\r\nHost: localhost:42069\r\nUser-Agent: curl/7.81.0\r\nAccept: */*\r\n\r\n"))
	require.NoError(t, err)
	require.NotNil(t, r)
	assert.Equal(t, "GET", r.RequestLine.Method)
	assert.Equal(t, "/coffee", r.RequestLine.RequestTarget)
	assert.Equal(t, "1.1", r.RequestLine.HttpVersion)

	// Test: Invalid number of parts in request line
	_, err = RequestFromReader(strings.NewReader("/coffee HTTP/1.1\r\nHost: localhost:42069\r\nUser-Agent: curl/7.81.0\r\nAccept: */*\r\n\r\n"))
	require.Error(t, err)
}
```

- 물론 명세서를 정확하게 파악하고 정확하게 구현하고 싶다면 단순하고 선언적인 테스트 코드를 먼저 작성하는 것이 좋습니다.
