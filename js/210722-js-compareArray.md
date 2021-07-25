# 210722-js-compareArray.md

## js에서 배열 비교하기

### JSON.stringify(배열)

서로 다른 두 배열의 값이 같은지는 JSON형태의 스트링으로 변환 후 비교한다.

일반 부등호는 사용할 수 없다. 그냥 부등호는 참조주소값을 비교하기 때문

```jsx
const a = [1, 2];
const b = [1, 2];

console.log(a === b); //false

console.log(JSON.stringify(a) === JSON.stringify(b)); // true
```
