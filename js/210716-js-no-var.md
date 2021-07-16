# 210716-js-no-var.md

## 변수와 상수

특정 이름에 특정 값을 담는 것 : 선언하다

변수(variable) : 바뀔 수 있는 값

`let a = 1;`

상수(constant) : 바뀌지 않는 값

`const b = 1;`

\*\* 선언을 할 때 타입을 지정해줄 필요는 없다. 그냥 변수 이름 앞에 let 혹은 const 만 붙여주면 됨.

cf) 자바에서 문자열을 선언할 때 `String test = "Hi";` `int testInt = 100;`

자바스크립트에서 선언할 때 `let test = "Hi";` `let testInt = 100;`

### var, 이젠 안녕 !

ES6 이전에는 변수, 상수 모두 var 키워드로 사용했지만, 현재는 권장하지 않는다.

IE 8,9 와 같은 구형 브라우저는 let, const를 인식하지 못하지만, 바벨이라는 도구를 사용해 최신 js문법을 구형 브라우저에서도 돌아갈 수 있도록 변환 작업을 하니 보통은 var를 사용하지 않는다고 문제가 되지 않는다.

**var 사용이 위험한 이유 1 :**

조건문 등 블록 안팎에서 같은 이름을 재선언하여 사용할 경우 var은 기존에 선언했던 값이 변할 수도 있다. 반면, let과 const 는 구분되어져 블럭 안팎에 영향을 주지 않는다.

```jsx
const constA = 1;
let letB = 7;
var varV = 5;

if (true) {
  const constA = 10000;
  console.log("조건문 안 : " + constA); // 조건문 안 : 10000

  let letB = 70000;
  console.log("조건문 안 : " + letB); // 조건문 안: 70000

  var varV = 50000;
  console.log("조건문 안 : " + varV); // 조건문 안: 50000
}
console.log("조건문 밖 : " + constA); // 조건문 밖 : 1
console.log("조건문 밖 : " + letB); // 조건문 밖 : 7
console.log("조건문 밖 : " + varV); // 조건문 밖 : 50000
```
