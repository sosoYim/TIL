# 210720-js-arFn-foreach-map.md

## 배열 내장함수 (값 찾기)

### indexOf, findIndex, find

첫번째 값을 반환한다. 값이 없을 경우 -1 반환

`**indexOf(searchElement [, fromIndex])` :** 배열 안에 있는 \*\***특정 값을 찾아 **인덱스 반환**.

searchElement : 찾고자하는 값

fromIndex : 해당 인덱스 이후로 찾는다. (음수시 뒤에서 몇번째부터)

---

`**findIndex(callbackFn)**` : 특정 조건(함수 이용)을 이용해 배열 안의 값을 찾아 **인덱스 반환**

---

`**find(callbackFn)**` : 특정 조건(함수 이용)으로 배열 안의 값을 찾아 **객체 그 자체 반환**

### filter

특정 값을 추출해서 새로운 배열을 만들 때 사용

```jsx
const tools = [
  {
    id: 1,
    text: "포토샵",
    done: true,
  },
  {
    id: 2,
    text: "일러",
    done: false,
  },
  {
    id: 3,
    text: "프리미어프로",
    done: true,
  },
];

const todo = tools.filter((todo) => !todo.done); //
```

### forEach, map, filter, findIndex, find 의 syntax

```jsx
//element는 현재 배열에서 처리 중인 값

// Arrow function
filter((element) => { ... } )
filter((element, index) => { ... } )
filter((element, index, array) => { ... } )

// Callback function
filter(callbackFn)
filter(callbackFn, thisArg)

// Inline callback function
filter(function callbackFn(element) { ... })
filter(function callbackFn(element, index) { ... })
filter(function callbackFn(element, index, array){ ... })
filter(function callbackFn(element, index, array) { ... }, thisArg)
```
