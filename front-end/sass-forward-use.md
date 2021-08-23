# @forward @use

## 사스를 이용해 css 문서 하나로 통합하기

사스의 @forward 와 @use 이용해 어떻게 하나의 파일로 스타일 문서를 통합하는지 알아보자.

**`@use`**는 Sass 파일을 다른 Sass파일로 불러올 때 사용한다. @use는 "모듈"이라고도 불린다.

`**@forward**`는 `@use`를 통해 불러온 Sass파일을 불러와 사용자가 단 하나의 엔트리 포인트 파일로 로드할 수 있도록 한다.

## 구조 예제

### 01. scss 하위 폴더에 폴더별로 사스 문서 묶기

sass하위 폴더는 각각 유사한 기능을 하는 스타일들로 묶여있다. base는 리셋에 관한 스타일, 컴포넌츠는 버튼, 폼 등의 컴포트에 관한 스타일, utils는 색, 폰트 등에 관한 스타일들이 있다. 이렇게 기능별로 묶은 스타일들을 각각 `_index.scss` 파일에서 @forward 로 묶는다.

```jsx

//base
@forward './../base/reset';
//components
@forward './../components/button';
@forward './../components/form';
//utils
@forward './../utils/font';
@forward './../utils/color';
```

이렇게 묶인 스타일은 이곳 저곳에서 임포트를 해야할 때, 각각의 큰 묶음으로 불러오면 편하다.

### 02. style.scss에서 한데 연결된 스타일 문서들 모으기

`style.scss`가 컴파일시 변환할 유일한 scss 파일이다. (파일 이름명 앞에 _가 붙은 파일은 컴파일 대상이 아니다.) 

```jsx
//style.scss
@use './base';
@use './utils';
@use './components/';
```

## 더 알아보기

- 사스의 컴파일 방법

## 참고링크

[Sass-lang : @use](https://sass-lang.com/documentation/at-rules/use)

[Sass-lang : @forward](https://sass-lang.com/documentation/at-rules/forward)

김데레사 강사님 영상자료