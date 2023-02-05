<aside>
⛔ 개념

</aside>

| 변수 선언 | js에서는 크게 const, var, let으로 가능 |
| --- | --- |
| const  | 상수 선언, 재할당X의 경우에 사용 |
| var  | 많은 문제가 있기 때문에 사용 X |
| let  | var의 문제점을 보완하기 위해 만들어짐 |
- **var의 문제점**
    var로 변수 선언 시 var 키워드 생략 가능
    - 예시를 통한 설명
        ```jsx
       name = 'gildong';
       console.log(name); // gildong 출력        
  var로 변수 선언 후 중복 선언 가능
    - 예시를 통한 설명
        ```jsx
       var name = 'gildong';
       console.log(name); // gildong 출력   
       var name = 'hong';
       console.log(name); // hong 출력 
  지역/전역 변수 구분 불가
    - 예시를 통한 설명
        ```jsx
       for (var i=0; i<5; i++)
       {
           console.log(i); // 1234출력
       }
       console.log(i); // 원래라면 i는 for문의 지역변수이기 때문에 오류가 나야하지만, var로 선언하면 5까지 출력해버림.
  변수 호이스팅
    - 예시를 통한 설명
        ```jsx
       console.log(name); // undefined 출력   
       var name = 'hong';
       console.log(name); // hong 출력 
<br>
💨 정리
**js에서는 변수가 생성되면 선언 -> 초기화 -> 할당 순으로 진행**
**위에서부터 아래로 읽는 것이 아니라, 선언된 변수를 먼저 확인 후 코드 진행**
<br>
예시에서, 두번째 줄에서 생성된 변수를 먼저 확인하고, 변수를 자체적으로 정의한 후에 첫번째줄부터 코드를 읽어나간다.
따라서 var로 선언하면 name이 두번째 줄에서 선언되었음에도 불구하고 첫번째 줄에서 오류가 아닌 undefined로 출력해버린다.

<br>

<aside>
➡️ 위의 모든 문제들을 let으로 사용하면 해결 가능!!