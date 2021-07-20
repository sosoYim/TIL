# 210720-js-arFn-reduce.md

## 배열 내장함수

### reduce

`**reduce(callbackFn, initialValue)**` 배열의 모든 요소들을 이용하여 연산을 한다.

callbackFn : 배열의 모든 요소들에 실행될 함수 (initialValue가 정의되지 않는다면 첫번째는 무시)

콜백 함수에는 다음의 네가지 인자가 사용될 수 있다.

- accumulator : initialValue가 지정되었다면 그 값을 처음으로 사용. 콜백함수의 리턴값으로 사용된다.
- currentValue : 현재 사용되고 있는 배열의 값
- index : 현재 위치한 배열의 인덱스 값
- array : 사용중인 배열

initialValue : 첫 번째 콜백 함수의 인자로 사용될 값. 지정하지 않는다면 배열의 첫번째 인자가 initialValue가되고, 이 값에 함수가 실행되지 않고 스킵한다. 만약 비어있는 배열이라면 initialValue를 지정하지 않았을 때 에러가 난다.

**예제1)** 총합, 평균

```jsx
//num 배열의 원소 총 합 구하기
const sum = num.reduce((accumulator, current) => accumulator + current, 0);
//num 배열의 평균값 구하기
const av = num.reduce((accumulator, current, index, array) => {
  if (index === array.length - 1) {
    //마지막 원소
    return (accumulator + current) / array.length;
  }
  return accumulator + current;
}, 0);
```

**예제2)** 배열 안의 각 요소가 몇 개씩 존재하는지 카운트하기

accumulator에 빈 객체를 지정하여 시작.

```jsx
const count = num.reduce((acc, current) => {
  if (acc[current]) {
    acc[current] += 1;
  } else {
    acc[current] = 1;
  }
  return acc;
}, {});
```
