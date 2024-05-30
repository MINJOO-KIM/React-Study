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
