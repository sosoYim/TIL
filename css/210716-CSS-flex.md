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
