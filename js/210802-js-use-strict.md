# 210802-js-use-strict.md

## 엄격한 모드로 자바스크립트 사용 (ECMA5 부터 사용가능)

자바 스크립트는 타 언어에 비해 굉장히 유연한(flex)한 언어다. 변수를 선언하기도 전에 사용할 수도 있고 프로토타입의 내용을 바꿀 수도 있으며 같은 이름의 매개변수도 지정할 수 있다. 이 외에도 많은flexable한 특징으로 인해 효율성이 떨어지고 오류 발생률이 높은 나쁜 코드를 작성할 위험이 크다.

엘리는 상단에 반드시 "user strict"; 모드를 지정해주라고 조언한다.

### 주요 특징

자바스크립트 상단에 `"user strict";` 를 지정해주면 다음과 같은 상황을 방지한다.

1. 기존에는 조용히 무시되던 에러들을 throwing (변수 선언 없이 사용 등등)
2. JavaScript 엔진의 최적화 작업을 어렵게 만드는 실수들을 바로잡는다. (비-엄격 모드보다 더 빨리 작동할 수도 있음)
3. 엄격 모드는 ECMAScript의 차기 버전들에서 정의 될 문법을 금지

- 모든 브라우저에서 사용 가능하지만, 버전이 맞지 않는 경우에도 String 이기 때문에 따로 에러가 발생하지는 않는다.

### 참고 링크

[MDN](https://developer.mozilla.org/ko/docs/Web/JavaScript/Reference/Strict_mode)

[드림코딩 엘리](https://www.youtube.com/watch?v=tJieVCgGzhs&list=PLv2d7VI9OotTVOL4QmPfvJWPJvkmv6h-2&index=2)
