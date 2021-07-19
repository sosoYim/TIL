# 210719-CSS-focus-within.md

## 가상 클래스 :focus-within

자식 input 이 focus될 때, 부모를 선택한다. 매우 유용!

```css
.inputbox:focus-within {
  border: 1px solid red;
}
```

```html
<div class="inputbox" id="inputbox_id">
  <img
    src="./images/UI/shape=letter.svg"
    alt="input_id_icon"
    class="input_icon letter"
  />
  <input
    type="text"
    name="id"
    id="input_id"
    class="input"
    placeholder="아이디(이메일)"
  />
</div>
```
