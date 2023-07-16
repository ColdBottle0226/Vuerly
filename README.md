# Vuerly
vue.js(nuxt) 마켓컬리 프로젝트

### 사용기술
Spring boot
Swagger-ui
mybatis
Spring Security

### 구현 기능
1. 베스트, 신상품
    - 컴포넌트 분리
        - props, $emit
    - 사이드메뉴 필터링 적용($emit으로 부모 컴포넌트에 전송)
    - 인기순,최신순.가격순 정렬
2. 통합검색
    - 브랜드
    - 상품명
    - 카테고리
3. 회원가입,로그인,아이디 찾기, 비밀번호 찾기
    - 회원가입
        - 유효성검사(정규식 이용)
        - 중복검사
        - 비밀번호 암호화(스프링 시큐리티 Bcrypt)
        - 회원 secret key(UUID)
    - 로그인(암호화된 비밀번호 비교 → 0 : 아이디 불일치, -1 : 비밀번호 불일치)
    - 아이디찾기(가입된 이름 여부 확인)
        - 휴대폰 인증(네이버 클라우드 sms api)
        - 이메일 인증(SMTP이용)
    - 비밀번호 초기화(가입된 아이디 여부 확인)
        - 휴대폰 인증
        - 이메일 인증
4. 리뷰 작성, 수정, 삭제
    - 주문 완료시 리뷰 작성 가능
    - 리뷰 작성시, (작성가능 → 작성완료로 수정)
    - 리뷰 수정
5. 회원정보 수정
6. 장바구니
    - 장바구니 수량 변경
    - 장바구니 상황에 따른 가격 변동
    - 장바구니 삭제
7. 고객센터
    - 공지사항
    - 자주하는 질문
    - 1:1문의
        - 1:1문의 등록
        - 1:1문의 수정
        - 1:1문의 삭제
8. 배송지 관리
    - 배송지 수정
![신상품](https://user-images.githubusercontent.com/84282676/220141765-225b4d88-0b09-486c-9afa-c17415b7534c.png)
![베스트](https://user-images.githubusercontent.com/84282676/220141777-245c551c-0f0c-46f2-b059-097dbaed5fc7.png)


## 구현 화면 
<details>
<summary>메인화면</summary>

|                                                          헤더                                                         |                                                          메인화면                                                          |
| :-----------------------------------------------------------------------------------------------------------------------------: | :-----------------------------------------------------------------------------------------------------------------------------: |
| <img src="https://user-images.githubusercontent.com/84282676/220140325-7d9a9e17-44c3-475c-a262-f30e4b9a4155.png" width="100%"/> | <img src="https://user-images.githubusercontent.com/84282676/220140342-daa8622d-06fe-4725-9888-6004697e64ae.png" width="100%"/> |

|                                                           메인화면                                                           |                                                           푸터                                                          |
| :-----------------------------------------------------------------------------------------------------------------------------: | :-----------------------------------------------------------------------------------------------------------------------------: |
| <img src="https://user-images.githubusercontent.com/84282676/220140244-34dac838-8bff-40be-a65f-266f91ea2c23.png" width="100%"/> | <img src="https://user-images.githubusercontent.com/84282676/220140232-10b94058-e805-4769-be18-2fa0640b7922.png" width="100%"/> |
</details>
<br />




