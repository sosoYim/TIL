# 210716-CSS-flex.md

## Flex 개요

**수평, 수직 정렬에 관한 속성**
기준점, 방향 등을 이용해 쉽게 레이아웃을 구성할 수 있게 하였다. 기존에 inline-block, flow를 사용하면서 가지던 불편함들 해소.

**display: flex** 속성을 가진 **부모 요소** container가 있고, 그의 **자식요소**들 (item)에 대한 정렬을 다양한 속성으로 설정할 수 있다.

- 주 축(main-axis), 교차 축(cross-axis)

  주축 : flex-dirextion으로 지정된 방향

  교차 축 : 주축의 반대

- 시작점(main-start), 끝 점(main-end)

  flex-direction에 따라 상하 좌우가 정해진다.

- 교차축의 시작점(cross-start), 교차축의 끝 점(cross-end)

  교차축이 row면 무조건 좌측이 cross-start, 우측이 cross-end

  교차축이 column이면 무조건 상단이 cross-start, 하단이 cross-end

## 부모 요소 container 에 들어갈 속성

```css
/* 부모 요소 container 에 들어갈 속성*/

display: flex; /* 컨테이너는 블럭 요소*/
display: inline-flex; /* 컨테이너는 인라인 요소*/

/* 정렬 방향 */
flex-direction: row;
/* row, row-reverse, column, column-reverse */

/* 여러줄 묶음 (줄바꿈 설정) */
flex-wrap: wrap;
/* default - nowrap. 한줄에 다 들어간다.*/
/* wrap, wrap-reverse */

/* 주축에 대한 정렬 방법*/
justify-content: flex-start;
/* flex-start, flex-end, space-between, space-around*/

/* 여러 줄일 때 교차축에서 아이템의 정렬 방법*/
align-content: flex-start;
/* !필수조건! 여러줄일 때 wrap */
/* !필수조건! 여백 있음 */
/* default - stretch. 늘어난다.*/
/* flex-start, flex-end, center, space-between, space-around*/

/* 한 줄일 때 교차축에서 아이템의 정렬 방법*/
align-items: flex-start;
/* default - stretch */
/* flex-start, flex-end, center(요소 기준), baseline(문자열 기준)*/
```

## 자식 요소 item에 들어갈 속성

```css
/* item의 순서 설정 */
order: 숫자;
/* 음수 가능. html순서보다 우선됨 */
/* order 값이 같을 경우 html 순서에 따름 */

/* 총 너비에서 각 item의 증가 너비 비율 설정 */
flex-grow: 숫자;
/* 가변하는 너비 설정시 사용 */
/* 예를 들어 아이템 3개가 각각 1, 3, 2의 flex-grow값을 가질 때 */
/* 각각 차지할 수 있는 영역 중 1/6, 3/6, 2/6너비를 차지한다. */
/* 함께 위치하는 다른 item들의 크기에 영향을 받는다.*/

/* 감소 너비 비율 설정 */
flex-shrink: 숫자
/* 줄어든 px중 비율에 따라 나눠 감소 */

/* item의 기본 너비 설정 (공간 분배 전)*/
flex-basis:
/* default - auto : 아이템의 컨텐트의 길이로 설정 */
/* flex-basis: 0 이어야 컨텐츠 내용 상관 없이 flex-grow등의 값을 지정 */

/* 단축 속성 */
flex: flex-grow, flex-shirnk, flex-basis;
/* !하지만! flex에 flex-basis를 적지 않으면 auto가 아닌 0을 기본값으로 설정한다. */
/* 각각의 기본 값 : 0 1 auto */

/* 전체가 아닌 개별 item의 정렬 방법 */
align-self: stretch;
/* align-item 보다 우선한다. */
/* align-item 속성값들 사용 가능 */
/* stretch, flex-start, flex-end, center(요소 기준), baseline(문자열 기준)*/
```
