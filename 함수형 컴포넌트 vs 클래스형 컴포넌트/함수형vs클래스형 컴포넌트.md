| 컴포넌트 | 사용자에게 보여지는 UI 요소를 구분하는 단위 |
| --- | --- |
| 함수형 컴포넌트  |  function 으로 정의하고 return 문에 jsx 코드를 반환 (화살표 함수로도 구현 가능) |
| 클래스형 컴포넌트  | class로 정의하고 render() 함수에서 jsx 코드를 반환 |

***

> 원래 클래스형 컴포넌트에서는 state(상태)를 사용할 수 있으며 각종 라이프사이클 및 메서드를 이용하여 컴포넌트가 마운트 혹은 언마운트 될 때 추가 작업을 수행시키는 등의 조작이 가능했었지만,
> `Hook`이 등장한 이후부터 함수형 컴포넌트에서도 대부분 구현이 가능하게 됨
> 
**➡ 함수형 컴포넌트로 사용 가능! 
(Hook의 등장으로 class 없이 리액트 사용 가능)**

***

- **함수형 컴포넌트**
    App.js에서 `import MyComponent from './MyComponent';` 로 불러온 후 `<MyComponent/>` 를 작성한 뒤 ` npm start`
    - 예시를 통한 설명
        ```jsx
       import React from "react";
        import "./App.css";
        
        const NameBox = () => {
          const name = "test";
          return <div>{name}</div>;
        };
        
        export default NameBox;    
- **클래스형 컴포넌트**
  
    - 예시를 통한 설명
        ```jsx
         import React, { Component } from "react";
        class NameBox extends Component {
          render() {
            const name = "react";
            return <div className="react">{name}</div>;
          }
        }
        
        export default NameBox; 
 
***

Hook 공식 문서(참고)
> Hook은 함수 컴포넌트에서 React state와 생명주기 기능(lifecycle features)을 “연동(hook into)“할 수 있게 해주는 함수입니다. Hook은 class 안에서는 동작하지 않습니다. 대신 class 없이 React를 사용할 수 있게 해주는 것입니다. (하지만 이미 짜놓은 컴포넌트를 모조리 재작성하는 것은 권장하지 않습니다. 대신 새로 작성하는 컴포넌트부터는 Hook을 이용하시면 됩니다.)
