### Contents

- [JSX](#JSX)
- [Element](#Element)
- [Componenet와 Props](#component와-props)

### JSX

- JavaScript와 XML/HTML 코드가 결합된 형태
- JSX를 사용하면 React 내부적으로 createElement라는 함수를 사용해 변환한다.
- `createElement` 함수의 파라미터
  - ![alt text](image.png)
- 장점
  - Injectino Attacks 방어
- 사용법
  - 태그의 속성에 값 넣기
    ```jsx
    // 큰 따옴표 사이에 문자열
    const element = <div tabIndex="0"></div>;
    // 중괄호 사이에 자바스크립트 코드
    const element = <img src={user.avatarUrl}></img>;
    ```

### Element

- 리액트 앱을 구성하는 가장 작은 블록
- 리액트 Element는 자바스크립트 객체 형태로 존재
- 컴포넌트 렌더링을 위해 모든 컴포넌트가 createElement 함수를 통해 Element로 변환된다.
- 특징
  - 불변성(immutable): Elements 생성 후에는 children이나 attributes를 바꿀 수 없다.
    - (Component: 붕어빵 틀, Elements: 구운 붕어빵들...)
    - 그럼 화면에 변경된 element를 보여줄 때는 어떻게 할까?
      -> 새로운 element를 만들어 기존 element가 연결되어 있는 부분에 바꿔서 달아주면 된다! (Virtual DOM)
- Element 렌더링하기
  - 루트 div에 React Element 렌더링하기
    - ![alt text](image-1.png)
    - ![alt text](image-2.png)
      > **React Element와 DOM Element의 차이** > <br/>React 엘리먼트는 React의 Virtual DOM에 존재하는 것이고 DOM 엘리먼트는 실제 브라우저의 DOM에 존재!
  - 렌더링된 Elements를 업데이트 하기
    - ![alt text](image-3.png)
    - 함수가 호출될 때마다 기존 엘리먼트를 변경하는 것이 아니라 새로운 엘리먼트를 생성해서 바꿔치기!

### Component와 Props

- 컴포넌트들이 모여서 페이지를 구성한다.(항상 대문자로 시작!)
- 입력: props / 출력: 리액트 element
- Props
  - 리액트 컴포넌트(붕어빵 틀) 의 속성 (붕어빵 재료)
  - 읽기 전용!! 값을 변경할 수 없다. (Read-only) 그러면....?
    - 새로운 값을 컴포넌트에 전달하여 새로 element를 생성하면 된다!
  - JSX: {}에 간단하게 props를 넣어줄 수 있다.
- Component 종류

  - 함수 컴포넌트
    ![alt text](image-4.png) - 리액트의 컴포넌트는 일종의 함수!

  - 클래스 컴포넌트
    ![alt text](image-5.png) - React.Component를 상속받아서 만들어!

- 컴포넌트 렌더링하기
  - 먼저, 컴포넌트로부터 엘리먼트를 만든다.
  - 그 엘리먼트를 렌더링한다.
    ![alt text](image-6.png)
- 컴포넌트 합성과 추출
    - 합성: 여러개의 컴포넌트로 새로운 컴포넌트를 만드는 것 
    - 추출: 복잡한 컴포넌트를 쪼개서 여러 개의 컴포넌트로 나누는 것 (재사용성)
    - 예제
        - Avatar, UserInfo 컴포넌트를 추출하여 Comment 컴포넌트에 반영하기
        ![alt text](image-7.png)
        ![alt text](image-8.png)
        ![alt text](image-9.png)


