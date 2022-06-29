# [3주차] 구조 분해 할당으로 props 가져오기


<aside>
⛔ 개념

</aside>

| 구조분해할당 | 배열이나 객체의 속성을 해체하여 그 값을 개별 변수에 담을 수 있게 하는 자바스크립트 표현식 |
| --- | --- |
| props | React가 컴포넌트를 발견하면 JSX 어트리뷰트를 해당 컴포넌트에 단일 객체로 전달하는데, 이 객체를 props(properties)라고 한다. |
- **구조분해할당**
    - 예시를 통한 설명
        
        [a, b, ...rest] = [10, 20, 30, 40, 50]; 에서 rest는 배열 [30,40,50]을 의미하게 된다.
        
    
    ```jsx
    let a, b, rest;
    
    [a, b] = [10, 20];
    
    console.log(a); // output: 10
    console.log(b); // output: 20
    
    [a, b, ...rest] = [10, 20, 30, 40, 50];
    
    console.log(rest); // output: [30,40,50]
    ```
    

- **props(properties)**
    
    어떠한 값을 컴포넌트에게 전달해줘야 할 때, props를 사용
    
    - 예시를 통한 설명
        
        App 컴포넌트에서 Hello 컴포넌트를 사용 할 때 `name` ,`color`라는 값을 전달해주고 싶다면, 아래와 같이 코드 작성
        
        - App.js
        
        ```jsx
        import React from 'react';
        import Hello from './Hello';
        
        function App() {
          return (
            <Hello name="react" color="red"/>
          );
        }
        
        export default App;
        ```
        
        - Hello.js
        
        ```jsx
        import React from 'react';
        
        function Hello(props) {
          return <div style={{ color: props.color }}>안녕하세요 {props.name}</div>
        }
        
        export default Hello;
        ```
        
        위와 같이 props 는 객체 형태로 전달되고, 만약 `name` ,`color`값을 조회하고 싶다면 `props.name`, `props.color`로 조회
        
    

---

<aside>
➡️ 구조분해할당을 이용한 props 사용

</aside>

- 예시를 통한 설명
    
    위의 예시인 Hello.js에서 함수의 파라메터에 구조분해할당을 이용하면, props 내부의 값을 조회 할 때마다 `props.` 을 입력하지 않아도 가능, 더 간결한 코드 사용 가능
    
    - Hello.js (구조분해할당사용X)
        
        Hello(props)로 함수 사용
        
    
    ```jsx
    import React from 'react';
    
    function Hello(props) {
      return <div style={{ color: props.color }}>안녕하세요 {props.name}</div>
    }
    
    export default Hello;
    ```
    
    - Hello.js(구조분해할당사용O)
        
        Hello({ color, name })로 함수 사용
        
    
    ```jsx
    import React from 'react';
    
    function Hello({ color, name }) {
      return <div style={{ color }}>안녕하세요 {name}</div>
    }
    
    export default Hello;
    ```