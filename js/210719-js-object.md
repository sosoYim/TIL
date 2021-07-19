# 210719-js-object.md

## 객체

[김민준 강사님 강의자료](https://learnjs.vlpt.us/basics/08-loop.html)

### 모양

js 에서 객체는, 키 : 값의 형태로 다양한 키값을 한 군데 묶었다. 키와 값의 사이는 쉼표(,)로 연결한다.

```jsx
const 객체이름 = {
		키(key) : 값(value),
		키2 : 값2,
		키3 : 값3
};

(예시)=========================================================
const apple = {
		color : red,
		taste : sweet
};

function print(fruit){
		const text = `This fruit is ${fruit.color} and it tastes ${fruit.taste}.`;
		console.log(text);
}
print(apple); //This fruit is red and it tastes sweet.

```

### 비구조 문법 (객체 구조 분해)

```jsx
//위에서 정의한 apple 객체를 비구조 문법 형태로 분해한 것 예시

const { color } = apple;

function print(fruit) {
  const { color, taste } = fruit;
  const text = `This fruit is ${color} and it tastes ${taste}.`;
  console.log(text);
}

function print({ color, taste }) {
  const text = `This fruit is ${color} and it tastes ${taste}.`;
  console.log(text);
}
```

### Getter 와 Setter

```jsx
getter : 특정 값을 **조회**하려고 할 때 사용하는 것
setter : 특정 값을 **설정**할 때 마다 사용하는 것

겟터 세터와 인스턴스를 구분해주기 위해서 _를 붙여준다.
세터에 특정 함수를 호출하여 값을 넣을 때마다 원하는 작업을 처리하게 할 수 있다.

const dog = {
	_name: '멍멍이',
	get name(){
		return this._name;
	}
	set name(value){
		console.log('이름이 바뀝니다..' + value);
		this._name = value;
	}
}
console.lgo(dog._name);
dog.name = '뭉뭉이';
console.log(dog._name);
```
