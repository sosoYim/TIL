# 210715-CSS-selector.md

## 선언방식

- 인라인 선언 : 선택자 필요 없이 스타일이 적용될 요소에 직접 입력
- 내장(embedded 방식) : HTML <head> 영역 안에 입력
- **선언 방식 :** head 영역에서 css 문서 가져오기 `<link rel="stylesheet" href="./css/main.css">`
- @import 방식 : css 내부에서 다른 css 문서 가져오기

## 선택자

### 기본 선택자

- 전체 선택자(Universal Selector)

```css
* {
  color: red;
}
```

- 태그 선택자(Type Selector)

```css
li {
  color: red;
}
```

- 클래스 선택자 (Class Selector)

HTML class 속성의 값

```css
.fruit {
  color: red;
}

/* html의 클래스 값이 fruit */
```

- id 선택자 (Id Selector)

```css
#banana {
  color: yellow;
}
```

### 복합 선택자

- **일치 선택자(Basic Combinator)**

선택자 두개를 동시에 만족하는 것

```css
span.orange {
  color: red;
}
```

- **자식 선택자 (Child Combinator)**

A > B (A의 자식 중 B)

```css
ul > .orange {
}
```

- **후손(하위) 선택자(Descendant Combinator)**

A B (A의 후손 요소 B를 선택)

```css
div .orange{
		color: red;
}

<div>
		<ul>
				<li>사과</li>
				<li class="orange">오렌지</li> /*선택*/
				<li>딸기</li>
				<li>망고</li>
				<li>키위</li>
		</ul>
</div>
```

- **인접 형제 선택자(Adjacent Sibling Combinator)**

A + B (A의 **다음 형제** 요소 B **하나** 선택)

```css
.orange + li {
		color: red;
}

<ul>
		<li>사과</li>
		<li class="orange">오렌지</li>
		<li>딸기</li> /*선택*/
		<li>망고</li>
		<li>키위</li>
</ul>
```

- **일반 형제 선택자(General Sibling Combinator)**

A ~ B (A의 **다음 형제** 요소 B **모두** 선택)

```css
.orange ~ li {
		color: red;
}

<ul>
		<li>사과</li>
		<li class="orange">오렌지</li>
		<li>딸기</li> /*선택*/
		<li>망고</li> /*선택*/
		<li>키위</li> /*선택*/
</ul>
```

### 가상 클래스 선택자(Pseudo-Classes Selectors

**:**

```css
a:hover {
  color: red;
}
```

E:**hover**

마우스 올릴 때

E:**active**

클릭하는 동안

E:**focus**

포커스된 동안에만

### 11-6. 가상 요소 선택자(Pseudo-Elements Selectors)

**::**

`**E::before` `E::after`\*\*

E요소 내부의 앞 혹은 뒤에, 내용(Content)를 삽입. content 속성을 꼭 넣어줘야 한다.

```css
ul {
  font-size: 40px;
}

ul li::before {
  content: ""; /*텍스트를 넣지 않더라도 꼭 넣어준다.*/
  background: tomato;
  width: 30px;
  height: 30px;
  display: inline-block;
  border-radius: 50%;
}

ul li::after {
  content: url("");
}
```
