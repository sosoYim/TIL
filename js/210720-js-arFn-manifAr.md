# 210720-js-arFn-manifAr.md

## 배열 내장함수 (조작, 추출)

**테스트 배열 num**

`const num = [10,20,30,20];`

### splice & slice

`**splice(start[, deleteCount[, item1[, item2[, ...]]]])**`

원본 배열을 삭제, 교체, 추가 하여 내용 변경.

start : 시작 index

deleteCount : 몇 개 삭제할 지

intem1,2 ... : start 인덱스부터 새로 추가할 원소

`**slice(begin [, end])**`

배열의 특정 부분을 추출한다. 원본 배열은 변하지 않는다.

begin : 시작 인덱스 (음수일 경우 뒤에서 몇번째~)

end : 끝 인덱스 (갯수 아님 주의)(끝 인덱스는 포함 안됨 주의)

```jsx
//num = [10,20,30,20]

const splices = num.splice(2, 0, 10000, 100000); //[10,20,10000,100000,30,20]
console.log(splices);
console.log(num);

const slice = num.slice(2, 3); //[30]
console.log(slice);
```

### shift, pop, unshift, push

`**shift()**` : 맨 앞에 있는 원소를 하나씩 뺀다.

`**unshift()**` : 맨 앞에 원소를 하나 추가한다.

---

`**pop()**` : 맨 뒤에 있는 원소를 하나씩 뺀다.

`**push()**` : 맨 뒤에 원소를 하나 추가한다.

### concat

`**concat()**` 두 배열을 하나로 이어 새로운 배열을 만든다. 기존의 배열은 건드리지 않는다.

\*\* 스프레드 연산자로도 구현 가능 [...arr1,...arr2]

### join

`**join(['seperator'])` :\*\* 배열을 하나의 문자열로 만들어 준다.

seperator : 배열의 원소 사이사이 들어갈 구분자

```jsx
//num = [10,20,30,20]
num.join("-"); //10-20-30-20
```
