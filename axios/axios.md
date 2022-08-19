<aside>
⛔ 개념

</aside>

| axios | 브라우저, Node.js를 위한 Promise API를 활용하는 HTTP 비동기 통신 라이브러리, 백엔드와 프론트엔드를 연결 |
| --- | --- |
| GET  | axios.get(url[, config]) |
| POST | axios.post(url, data[, config]) |
| PUT  | axios.put(url, data[, config]) |
| DELETE  | axios.delete(url[, config]) |
- **GET**
    데이터를 요청 (데이터를 가져온다고 생각하면 간편)
   - 단순 데이터 (ex.페이지) 요청의 경우 
        - 예시를 통한 설명
        ```jsx
       export const getFriendList = () => getAxios('/friend/list');        
  - 파라메터를 이용한 데이터 요청의 경우
    - 예시를 통한 설명
        ```jsx
       export const acceptFriend = (targetUserId) =>
           getAxios(`/friend/request/accept/${targetUserId}`);

- **POST**
    데이터를 전송 (보통 데이터를 Message Body에 포함시켜 전송)
    - 예시를 통한 설명
        ```jsx
       export const sendFriendRequest = (targetUserId) =>
            postAxios(`/friend/request/${targetUserId}`);        
            
- **PUT**
    데이터를 수정 (POST와 비슷)
    - 예시를 통한 설명 (우리 프로젝트에 PUT이 사용되지 않았으므로 외부에서 예시를 가져왔다.)
        ```jsx
       axios.put("url", {
        username: "",
        password: ""
        })
        .then(function (response) {
             // response  
        }).catch(function (error) {
            // 오류발생시 실행
        })   
  
- **DELETE**
    데이터베이스에 저장되어 있는 내용을 삭제
    - 예시를 통한 설명
        ```jsx
       export const deleteFriend = (targetUserId) => {
           deleteAxios(`/friend/delete/${targetUserId}`);
        };     
            
<br>
💨 나의 언어로 정리
**AXIOS의 사용에는 GET, POST, PUT, DELETE가 있는데, 각각 데이터를 가져올 때(요청), 전송할 때, 수정할 때, 삭제할 때 사용한다.**
<br>
