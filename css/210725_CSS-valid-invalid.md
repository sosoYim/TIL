# 210725_CSS-valid-invalid.md

## 가상 클래스 :valid :invalid

input 태그에 required, email ... 의 조건이 있을 때 이에 대한 valid, invalid 상태를 선택하여 스타일을 지정할 수 있다.

```css
.input:valid {
  border: 1px solid black;
}

.input:invalid {
  border: 1px solid red;
}
```

```html
<input type="text" name="id" class="input" placeholder="아이디(이메일)" />
```
