# TIL

1일1커밋 무사고: 222일차

00:00

## todo

- [ ] 기간별 제목 & 카드 묶음
- [ ] request waterfall 해결
- [ ] nav 라우트를 활용해서 상태관리하기
- [ ] axios interceptor 동작 실패
- [ ] 경고 modal
- [ ] 이메일 저장하기
- [x] 버틈 컴포넌트 리팩토링
- [x] 주간회고
- [x] 이번주 배운 내용 정리
- [x] PR marge

## 잡생각

- 개발자로서 내공을 잘 보여줘야 합니다.

### 잘하기 위해 필요한 것과 재미있게 하고 싶은 것이 다른 상황은 어떻게 해야 하는가?

- 이력서를 정리해야 하는데 블로그 관리를 더 하고 싶습니다.

## 주간 회고

|  요일  | 시간  |
| :----: | ----- |
| 월요일 | 05:11 |
| 화요일 | 06:41 |
| 수요일 | 04:29 |
| 목요일 | 04:50 |
| 금요일 | 03:43 |
| 토요일 | 00:00 |
| 일요일 | 04:39 |
|   합   | 29:33 |

컨디션 관리를 잘하도록 합시다.

### Liked

- 침묵을 제거할 수 있는 podcast들을 발견했습니다. 더이상 넷플릭스에 의존할 필요가 없어졌습니다.

### Learned

- 지난 분기에 비해서 발전한 것이 현격히 없습니다.
  - 너무 게으르게 살아서 남들보다 못해졌습니다. 평균 이하의 실력을 원래 갖고 있었습니다. 하지만 만회할 기회를 자꾸 놓칩니다.
- 생활이 규칙적이다고 무조건 더 생산적인 것은 아닙니다.
  - 생산성은 규칙적인 생활 속에서 해결할 과제 선정과 시간관리가 중요합니다.

### Lacked

- 프로젝트의 끝이 보인다고 자꾸 착각합니다. 다음 핵심 기능이 또 남아있습니다. 카드의 덱들을 분류하는 것입니다.
- 지난주에 잘하기 위해 필요하다는 것은 생각만하고 말았습니다. 생각은 의미가 없습니다.
  - 실천으로 옮겨진 것이 없습니다.

### Longed(잘하기 위해 필요한 것)

- 개발자로서 특이한 개발경험을 강조해야 합니다.
- 프로젝트가 끝나면 특이한 개발 경험들을 정리하고 보여줘야 합니다.
- 프로젝트가 완료되는 시점에 스터디를 구해야 합니다.
- 이력서를 다듬어야 합니다.
  - 효율적이고 빠른 편집이 가능해야 합니다.
  - 노션은 링크 문제가 너무 많습니다.
- 프로젝트가 완료되었지만 완료되었다고 착각하지 말아야 합니다.
- 의욕관리를 해야 합니다. 장시간 집중하고 생산적인 결과를 만들 수 있는 마인드 셋을 갖추어야 합니다. 설령 혼자 올바르다고 생각하는 방식이라도 활용해야 합니다.
- 사이드 프로젝트와 취업을 위한 공부 이외에 프로그래밍을 잘하기 위한 학습을 또 해야 합니다.

### Action Item

- [ ] axios interceptor 동작 실패 해결
  - [ ] 해결 후 문서화
- [ ] 기간별 제목 & 카드 묶음
  - [ ] 엣지케이스와 리팩토링 처리
- [ ] request waterfall 해결
  - [ ] react-query 응용
- [ ] nav 라우트를 활용해서 상태관리하기
- [ ] 경고 modal
- [ ] 이메일 저장하기

## 버튼 리팩토링

```tsx
import styled from '@emotion/styled';
import { Link } from 'react-router-dom';

type HierarchyType = 'primary' | 'secondary' | 'ghost';
type ColorType = 'green' | 'red' | 'neutral';

type ButtonWrapperProps = {
  width?: number | 'grow';
  disabled?: boolean;
  hierarchy: HierarchyType;
  isLoading: boolean;
  color: ColorType;
};

export const ButtonWrapper = styled.div<ButtonWrapperProps>`
  border-radius: 0.5rem;
  height: 2.75rem;
  min-width: 5.25rem;

  position: relative;

  display: flex;
  justify-content: center;
  align-items: center;

  width: ${(props) => {
    // 숫자 입력시 숫자만큼 채우기
    if (!props.width) return 'fit-content';
    if (props.width !== 'grow') return (props.width / 16).toString() + 'rem';
    return 'fit-content';
  }};

  ${(props) => props.width === 'grow' && 'flex: 1 1 0px;'}

  button,
  a {
    all: unset;

    width: 100%;
    height: 100%;
    border-radius: 0.5rem;

    background-color: ${(props) => {
      if (props.hierarchy === 'secondary') {
        return props.theme.colors.white;
      }

      if (props.hierarchy === 'ghost') {
        return props.theme.colors.white;
      }

      if (props.disabled && !props.isLoading && props.hierarchy === 'primary')
        return props.theme.colors.gray400;

      if (props.disabled && !props.isLoading && props.hierarchy !== 'primary')
        return props.theme.colors.white;
      if (props.color === 'green') return props.theme.colors.green500;
      if (props.color === 'red') return props.theme.colors.red500;
      if (props.color === 'neutral') return props.theme.colors.gray700; // 컬러 미정
    }};

    box-shadow: 0 0 0 2px ${(props) => {
        if (props.hierarchy === 'secondary') {
          if (props.disabled) return props.theme.colors.gray400;
          else {
            if (props.color === 'green') return props.theme.colors.green500;
            if (props.color === 'red') return props.theme.colors.red500;
            if (props.color === 'neutral') return props.theme.colors.gray700; // 컬러 미정
          }
        } else {
          return 'none';
        }
      }} inset;

    ${(props) => props.theme.fonts.body16Regular}

    display: flex;
    justify-content: center;
    align-items: center;

    :focus-visible {
      box-shadow: 0 0 0 0.25rem ${(props) => {
          if (props.color === 'green') return props.theme.colors.green200;
          if (props.color === 'red') return props.theme.colors.red200;
          if (props.color === 'neutral') return props.theme.colors.gray400;
        }} inset;
    }

    :hover {
      background-color: ${(props) => {
        if (props.disabled) return props.theme.colors.gray400;
        if (props.hierarchy === 'primary') {
          if (props.color === 'green') return props.theme.colors.green400;
          if (props.color === 'red') return props.theme.colors.red400;
          if (props.color === 'neutral') return props.theme.colors.gray600;
        } else {
          if (props.color === 'green') return props.theme.colors.green050;
          if (props.color === 'red') return props.theme.colors.red050;
          if (props.color === 'neutral') return props.theme.colors.gray100;
        }
      }};
    }

    :active {
      background-color: ${(props) => {
        if (props.disabled) return props.theme.colors.gray400;
        if (props.hierarchy === 'primary') {
          if (props.color === 'green') return props.theme.colors.green600;
          if (props.color === 'red') return props.theme.colors.red600;
          if (props.color === 'neutral') return props.theme.colors.gray800;
        } else {
          if (props.color === 'green') return props.theme.colors.green100;
          if (props.color === 'red') return props.theme.colors.red100;
          if (props.color === 'neutral') return props.theme.colors.gray200; // 컬러 미정
        }
      }};
    }
  }
`;

type CustomLinkProps = Pick<ButtonWrapperProps, 'disabled'>;

export const CustomLink = styled(Link)<CustomLinkProps>`
  ${(props) => !props.disabled && 'cursor: pointer;'}
`;

export const CustomButton = styled.button``;

type TextWrapperProps = Omit<ButtonWrapperProps, 'width'>;

export const TextWrapper = styled.span<TextWrapperProps>`
  white-space: nowrap;
  overflow: hidden;
  text-overflow: ellipsis;
  max-width: 100%;
  color: ${(props) => {
    if (props.isLoading) return 'transparent';
    if (props.disabled && props.hierarchy !== 'primary')
      return props.theme.colors.gray400;
    if (props.hierarchy === 'primary') return props.theme.colors.white;
    if (props.color === 'green') return props.theme.colors.green500;
    if (props.color === 'red') return props.theme.colors.red500;
    if (props.color === 'neutral') return props.theme.colors.gray700;
    return props.theme.colors.green500;
  }};
  margin: 0 1rem;
`;

export const LoaderWrapper = styled.div`
  position: absolute;
  top: 0;
  left: 0;
  right: 0;
  bottom: 0;
  display: flex;
  align-items: center;
  justify-content: center;
`;
```

```tsx
import styled from '@emotion/styled';
import { Link } from 'react-router-dom';

type HierarchyType = 'primary' | 'secondary' | 'ghost';
type ColorType = 'green' | 'red' | 'neutral';

type ButtonWrapperProps = {
  width?: number | 'grow';
  disabled?: boolean;
  hierarchy: HierarchyType;
  isLoading: boolean;
  color: ColorType;
};

export const ButtonWrapper = styled.div<ButtonWrapperProps>`
  border-radius: 0.5rem;
  height: 2.75rem;
  min-width: 5.25rem;

  position: relative;

  display: flex;
  justify-content: center;
  align-items: center;

  width: ${(props) => {
    // 숫자 입력시 숫자만큼 채우기
    if (!props.width) return 'fit-content';
    if (props.width !== 'grow') return (props.width / 16).toString() + 'rem';
    return 'fit-content';
  }};

  ${(props) => props.width === 'grow' && 'flex: 1 1 0px;'}

  button,
  a {
    all: unset;

    width: 100%;
    height: 100%;
    border-radius: 0.5rem;

    background-color: ${(props) => {
      if (props.hierarchy !== 'primary') return props.theme.colors.white;

      if (props.disabled && !props.isLoading) {
        if (props.hierarchy === 'primary') return props.theme.colors.gray400;
        else return props.theme.colors.white;
      }

      const colorMap = {
        green: props.theme.colors.green500,
        red: props.theme.colors.red500,
        neutral: props.theme.colors.gray700,
      };

      return colorMap[props.color];
    }};

    box-shadow: 0 0 0 2px ${(props) => {
        if (props.disabled && props.hierarchy === 'secondary')
          return props.theme.colors.gray400;

        const colorMap = {
          green: props.theme.colors.green500,
          red: props.theme.colors.red500,
          neutral: props.theme.colors.gray700,
        };

        if (props.hierarchy === 'secondary') return colorMap[props.color];

        return 'none';
      }} inset;

    ${(props) => props.theme.fonts.body16Regular}

    display: flex;
    justify-content: center;
    align-items: center;

    :focus-visible {
      box-shadow: 0 0 0 0.25rem ${(props) => {
          const colorMap = {
            green: props.theme.colors.green200,
            red: props.theme.colors.red200,
            neutral: props.theme.colors.gray400,
          } as const;

          return colorMap[props.color];
        }} inset;
    }

    :hover {
      background-color: ${(props) => {
        if (props.disabled) return props.theme.colors.gray400;

        const colorMap = {
          primary: {
            green: props.theme.colors.green400,
            red: props.theme.colors.red400,
            neutral: props.theme.colors.gray600,
          },
          secondary: {
            green: props.theme.colors.green050,
            red: props.theme.colors.red050,
            neutral: props.theme.colors.gray100,
          },
          ghost: {
            green: props.theme.colors.green050,
            red: props.theme.colors.red050,
            neutral: props.theme.colors.gray100,
          },
        } as const;

        return colorMap[props.hierarchy][props.color];
      }};
    }

    :active {
      background-color: ${(props) => {
        if (props.disabled) return props.theme.colors.gray400;

        const colorMap = {
          primary: {
            green: props.theme.colors.green600,
            red: props.theme.colors.red600,
            neutral: props.theme.colors.gray800,
          },
          secondary: {
            green: props.theme.colors.green100,
            red: props.theme.colors.red100,
            neutral: props.theme.colors.gray200,
          },
          ghost: {
            green: props.theme.colors.green100,
            red: props.theme.colors.red100,
            neutral: props.theme.colors.gray200,
          },
        } as const;

        return colorMap[props.hierarchy][props.color];
      }};
    }
  }
`;

type CustomLinkProps = Pick<ButtonWrapperProps, 'disabled'>;

export const CustomLink = styled(Link)<CustomLinkProps>`
  ${(props) => !props.disabled && 'cursor: pointer;'}
`;

export const CustomButton = styled.button``;

type TextWrapperProps = Omit<ButtonWrapperProps, 'width'>;

export const TextWrapper = styled.span<TextWrapperProps>`
  white-space: nowrap;
  overflow: hidden;
  text-overflow: ellipsis;
  max-width: 100%;
  color: ${(props) => {
    if (props.isLoading) return 'transparent';
    if (props.disabled && props.hierarchy !== 'primary')
      return props.theme.colors.gray400;
    if (props.hierarchy === 'primary') return props.theme.colors.white;

    const colorMap = {
      green: props.theme.colors.green500,
      red: props.theme.colors.red500,
      neutral: props.theme.colors.gray700,
    } as const;

    return colorMap[props.color];
  }};
  margin: 0 1rem;
`;

export const LoaderWrapper = styled.div`
  position: absolute;
  top: 0;
  left: 0;
  right: 0;
  bottom: 0;
  display: flex;
  align-items: center;
  justify-content: center;
`;
```

맵핑 패턴을 적용으로 조금더 가독성을 확보할 수 있습니다. 코드의 중복이 있는데 중복보다는 가독성이 더 중요합니다.

## 기간별 제목 & 카드 묶음

- 제목 추가하기
- 구간 분류하고 배열에 보관하기
