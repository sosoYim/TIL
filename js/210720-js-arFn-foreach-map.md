# 210720-js-arFn-foreach-map.md

## 배열 내장함수

### forEach

`**forEach(callbackFn)**` :배열의 모든 요소들을 돌며 특정 코드를 실행한다.

```jsx
const fruit = ["apple", "banana", "mango"];

//forEach 예제 1 :
function print(thing) {
  console.log(thing);
}

fruit.forEach(print);

//forEach 예제2 :
fruit.forEach(function (thing) {
  console.log(thing);
});

//forEach 예제3 :
fruit.forEach((thing) => {
  console.log(thing);
});
```

### map

`**map(callbackFn)` :** 배열 각각의 요소에 함수를 적용시켜 전체적으로 **변환\*\*할 때 사용

```jsx
const array = [2, 4, 5, 6];
const suqare = (n) => n * n;
const squared = array.map(suqare);
//const squared = array.map(n=>n*n);
```
