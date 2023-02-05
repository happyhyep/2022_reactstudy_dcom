# [2주차] SPA vs MPA

<aside>
⛔ 정의

</aside>

| SPA | Single Page Application : 한 개의 page로 구성된 application |
| --- | --- |
| MPA | Multi Page Application : 여러 개의 page로 구성된 application |
- SPA
    - 설명
        
        웹 애플리케이션에 필요한 모든 정적 리소스를 최초로 한번에 다운로드
        새로운 요청이 있으면 페이지 갱신에 필요한 데이터만 전달받아 페이지를 갱신
        CSR(Client Side Rendering) 이라고도 함
        
- MPA
    - 설명
        
        새로운 페이지를 요청할 때마다 정적 리소스 다운로드
        전체 페이지 계속해서 다시 렌더링
        SSR(Server Side Rendering) 이라고도 함
        

---

<aside>
❓ 사진으로 이해하기

</aside>

- MPA, SPA
    - 이미지
        
        ![Untitled](%5B2%E1%84%8C%E1%85%AE%E1%84%8E%E1%85%A1%5D%20SPA%20vs%20MPA%209c3e6dbd67ec483e8e14d0c29d09a847/Untitled.png)
        

<aside>
➡️ 장점

</aside>

- SPA
    - 장점
        - 사용자 경험 측면
            1. 전체 페이지 업데이트 필요 X → 속도 빠름
            2. 전체 페이지 업로드 과정에서 깜박거림 X
            3. application 반응 빠름
        
        - 개발자 측면
            1. 서버 사용 필요 X
            2. 크롬 디버깅 easy
            3. 로컬 데이터의 효과적 cache
- MPA
    - 장점
        - SEO 측면
            1. 완성된 형태의 html 파일 전달 → 검색 엔진이 페이지 크롤링 하는데 적합
        

---

<aside>
➡️ 단점

</aside>

- SPA
    - 단점
        - 초기 구동 속도 측면
            1. 초기에 모든 정적 리소스를 다 받음 → 초기 구동 속도는 느림
        
        - SEO 측면
        
- MPA
    - 단점
        - 사용자 경험 측면
            1. 새로운 페이지로 이동 시 깜박거림 O
        
        - 개발자 측면
            1. 프론트엔드와 백엔드의 연관이 높음 → 개발 복잡
        

---