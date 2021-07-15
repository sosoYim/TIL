# 210715-CSS-background.md

## background

백그라운드 관련 다양한 속성. 오늘의 포인트는

background-attachment: fixed;

웹사이트에서 이미지 하나가 배경에 붙어있고 다른 구역들은 내려가는 (?) 멋진 느낌이 바로 이 속성이었다!

```css
background-size: auto 100%; /*가로 맞춤*/

/* 이미지 삽입(개별 속성) */
/* background-repeat: 디폴트 값이 repeat */
backgroung-image: url("../img/11.jpg"),
url("../img/12.jpg");

/* 다중 이미지 삽입 */
background: url("../img/11.jpg") no-repeat,
url("../img/12.jpg") no-repeat 100px 50px,
url("../img/13.jpg") repeat-x;

먼저 삽입한 이미지가 가장 위에 있다.

repeat: repeat-x 수평으로 반복

repeat: repeat-y 수직으로 반복

repeat: no-repeat 반복안함

/*==================================*/

background-position: 배경이미지의 위치 설정
% 왼쪽 상단 : 0% 0% / 오른쪽 하단 100% 100%
background-position: 0% 0%

방향일 경우앞뒤 바꿔도 됨
background-position: right bottom;
값이 단위(%, px 등)인 경우
앞 뒤 안 바꿔도 됨

방향과 단위를 함께 쓸 때는 방향은 x, y 위치에 맞춰 적어줘야한다.
(x좌우, y상하)
(left, 50%) / (40px, bottom)

/*============== background-attachment ====================*/
background-attachment: scroll 기본값
background-attachment: fixed; 이미지는 고정된채로 스크롤 내려감 (웹사이트에서 자주 사용)
background-attachment: local; 요소 내 스크롤 시 배경 이미지가 같이 스크롤 됨

/*============== background-size ===============*/
(가로, 세로)
background-size: 200px; /*찌그러지지 않게 가로값 하나만 적는 것도 추천*/
background-size: auto, 400px;
background-size: contain; /*요소의 짧은 너비에 맞추기*/

```
