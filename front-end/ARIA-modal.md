# Alert dialog (Modal)

얼럿 메세지를 포함하고 있는 다이얼로그, 첫 포커스가 다이얼로그의 요소로 가 있다.

얼럿 다이얼로그는 모달로 자주 불리는데, 유저에게 메세지를 띄우면서도 유저의 '응답'을 받아 일방적으로 메세지를 띄우는 얼럿과는 차이점이있다. 즉, 메세지를 띄우는 얼럿과 입력을 받는 다이얼로그의 기능을 함께 가졌다고 볼 수 있다.

모달창 생성시 개발자가 꼭 해야 하는 것:

1. 모달창이 떠있는 동안은 키보드와 마우스 사용이 모달창 내부 요소에만 사용할 수 있다. aria-modal
2. 모달창이 떴을 때, 포커스는 반드시 모달창의 활성화된 요소(인풋창, 버튼 등)에 지정돼있어야 한다.
3. The user agent SHOULD fire a system alert event through the accessibility API when the alert is created, provided one is specified by the intended accessibility API.

4. 개발자는 반드시 aria-describedby 로 얼럿 메세지를 참조해야한다. 그렇지 않다면 기기 내부적으로 해당 메세지를 정달할 수 있는 메커니즘이 있어야 한다.
