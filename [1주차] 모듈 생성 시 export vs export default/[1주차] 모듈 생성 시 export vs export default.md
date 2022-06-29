# [1주차] 모듈 생성 시 export vs export default ?

생성일: 2022년 4월 13일 오후 2:16
작성자: 정혜인
태그: JS

<aside>
⛔ 들어가기 전

</aside>

<<<<<<< HEAD
| 모듈? | 분리된 파일 / 일반적으로, 클래스 하나 혹은 복수의 함수로 구성된 라이브러리 하나로 구성 |
=======
| 모듈? | 분리된 파일 일반적으로, 클래스 하나 혹은 복수의 함수로 구성된 라이브러리 하나로 구성 |
| --- | --- |
>>>>>>> 5440526cdc990ebb9668b2918831f2de53e91cd3
| export | 변수나 함수 앞에 붙이면 외부 모듈에서 해당 변수나 함수에 접근 가능 |
| import | 외부 모듈의 기능을 가져옴 |

---

<aside>
❓ export 사용법

</aside>

- 변수나 함수, 클래스 맨 앞에 `export` 붙이기
    - example (열어서 보기)
        
        ```jsx
        배열 내보내기
        *export* let months = ['Jan', 'Feb', 'Mar','Apr', 'Aug', 'Sep', 'Oct', 'Nov', 'Dec'];
        
        상수 내보내기
        *export* const MODULES_BECAME_STANDARD_YEAR = 2015;
        
        클래스 내보내기
        *export* class User {
          constructor(name) {
            this.name = name;
          }
        }
        ```
        

- 선언부와 떨어진 곳에 `export` 붙이기
    - example (열어서 보기)
        
        ```jsx
        function sayHi(user) {
          alert(`Hello, ${user}!`);
        }
        
        function sayBye(user) {
          alert(`Bye, ${user}!`);
        }
        
        export {sayHi, sayBye}; // 두 함수를 내보냄
        ```
        

<aside>
➡️ import 사용법

</aside>

- 예시와 같이 목록을 만들어  `import{...}` 작성
    - example (열어서 보기)
        
        ```jsx
        import {sayHi, sayBye} from './say.js';
        
        sayHi('John'); // Hello, John!
        sayBye('John'); // Bye, John!
        ```
        

---

<aside>
❓ export default 사용법

</aside>

- 일반적으로 개체 하나만 선언되어있는 모듈을 만드는 것을 선호하기 때문에  `export default` 를 사용하여 ‘해당 모듈엔 개체가 하나만 있다’는 사실을 명확히 나타냄 (예시 참고)
    - example (열어서 보기)
        
        ```jsx
        export default class User { // export 옆에 'default'를 추가됨
          constructor(name) {
            this.name = name;
          }
        }
        ```
        

<aside>
➡️ import 사용법 (export default 일 경우)

</aside>

- `export default` 를 사용하면 중괄호 {} 없이 `import` 가능 (예시 참고, 위 import 사용법과 비교)
    - example (열어서 보기)
        
        ```jsx
        import User from './user.js'; // {User}가 아닌 User로 클래스를 가져옴
        
        new User('John');
        ```
        

💢 default export는 가져오기 할 때 내보내기 한 이름과 똑같아야 한다는 제약이 없음, 비슷하게 이름을 지으면 혼란의 여지 O

---
