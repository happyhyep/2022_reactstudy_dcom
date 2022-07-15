<aside>
⛔ 개념

</aside>

| state | 리액트 컴포넌트에서 동적인 값 |
| --- | --- |
| useState()  | 함수형 컴포넌트에서도 상태 관리 가능 |
- **useState()**
    
    - 예시를 통한 설명
        
       
        
        - App.js
        
        ```jsx
        function App() {
        const [counter, modifier] = React.useState(0);
        {/* const data = React.useState(0)과 같음 */}
        return (
      <div>
        <h3>Total Clicks : {counter}</h3>
        <button>Click me</button>
      </div>
        );
    }
        
useState() 를 호출하면 배열을 반환하는데,
첫번째 원소 counter는 현재 상태 값 변수이고, 
두번째 원소 modifier는 상태 값을 갱신해주는 setter 함수이다.
useState(0)으로 사용했는데, 괄호 안의 값은 상태의 초기값이다.
<br>
*const [myFavFood,mySecFavFood] = ["tomato","potato"]문법을 이용한 것이다. (리스트 내용을 변수에 바로 저장할 수 있음)*
<br>
<aside>
정리 ➡️ **React.useState() 함수 : [초기값, 실행할 function]의 리스트 형태**
