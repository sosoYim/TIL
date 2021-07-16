# 210716-js-function-declarations.md

## 함수 선언

### 기존 함수 선언 function declaration

```jsx
function hello(name) {
  console.log(name + ", hi!");
}

hello("Jake"); // Jake, hi!
```

function 함수이름(파라미터1,2,3...){코드 (및 return)}

실행방법 : 함수이름(파라미터1, 2,3...);

\*\* return은 값을 반환하고 함수를 종료하기 때문에 function 블럭 내에서 단 한번, 마지막에 위치해야 한다. (조건문에 들어가는 경우 제외)

### Arrow function 화살표 함수

ECMA 6에서 나온 새로운 함수 선언 방법. 매우 간결하다.

```jsx
const add = (a, b) => {
  return a + b;
};

const add = (a, b) => a + b;

const hello = (name) => {};
```

기존의 함수 선언 방식과 화살표 함수 선언 방법은 this 의 정의가 다르다. 이 부분은 다음 시간에...

(보너스) ES6 이후로 사용 가능한 유용한 `` : 연산자를 사용하지 않고 간단하게

```jsx
function hello(name) {
  return `Hello ${name}!`;
}
```
