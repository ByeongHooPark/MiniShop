# MiniShop -2인프로젝트, 상품페이지담당

<br/><br/><br/>
# :zap: 프로젝트소개
<br/>

### 간단한 마트 쇼핑몰을 구현하였습니다. 저는 상품페이지를 담당했습니다.

<br/>

<img src="https://github.com/ByeongHooPark/MiniShop/assets/123047580/070cbe00-5579-48d6-90e9-4ca2869dabbb"  width="300" height="300"/>

<br/><br/><br/><br/>

# :zap: 주요 기능설명

<br/>

##  1. 상품 리스트 페이지 - 조회 로직 일원화, 검색창 상품 리스트 임시호출

<br/><br/>

#### a. 전체조회, 카테고리 조회, 검색 조회와 각각의 더보기 페이징의 로직을 일원화 했습니다.

<br/>

<img src="https://github.com/ByeongHooPark/MiniShop/assets/123047580/070cbe00-5579-48d6-90e9-4ca2869dabbb"  width="300" height="300"/>

<br/><br/>

#### b. 검색창에 문자를 입력하면 한글 자모단위로 검색창이 상품 리스트를 임시 출력하도록 했습니다.

<br/>

<img src="https://github.com/ByeongHooPark/MiniShop/assets/123047580/bdd546d8-94ec-4a0f-8eac-d6caf94da36b"  width="300" height="300"/>

<br/><br/><br/><br/>

> #### 관련 코드
> #### 공통 - list 페이지 뷰 : /product-html/list.html
> 
> #### a. 조회 로직
> #### /product-js/list.js 의 getProduct()을 중심으로 readyfunction-전체, cateClicked()-카테고리,  searchProducts()-검색, moreButton()-더보기
> #### /product-java/ProductServiceProcess.java 의 getProduct() 메서드
>
> #### b. 검색창 로직
> #### /product-js/list.js 의 tempPrint()
> #### /product-java/ProductServiceProcess.java 의 searchProduct() 메서드

<br/><br/><br/><br/>

##  2. 장바구니 로직 - 그 중 비회원이 장바구니에 물건을 넣고 로그인 할 때

<br/><br/>

#### 비회원 장바구니는 쿠키와 세션으로, 회원 장바구니는 DB를 사용해서 데이터를 저장했습니다.
#### 로그인 성공시 로그인 successful handler로 비회원 장바구니 내역을 회원 장바구니 내역으로 옮겨 저장합니다.

<br/><br/><br/><br/>

> #### 관련 코드
> 
> #### /product-java/CustomAuthenticationSuccessHandler.java 의 '//쿠키 확인' 주석으로 시작해서 첫 for문까지
> #### /product-java/ProductServiceProcess.java 의 moveBasket() 메서드
























