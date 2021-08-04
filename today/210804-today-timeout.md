# 210804-today-3rd-week.md

## TIL

### 알고리즘

### Disjoint-set (서로소 집합)

중복되지 않는 부분집합들에 대한 정보를 저장하고 관리하는 자료구조.

Union-find : Disjoint-set을 위한 대표적인 알고리즘

```jsx
function Find(v) {
  if (v === unf[v]) return v;
  else return (unf[v] = Find(unf[v]));
}

function Union(a, b) {
  let fa = Find(a);
  let fb = Find(b);
  if (fa !== fb) unf[fa] = fb;
}
```

### 최소 스패닝 트리(크루스칼, union&find)

순환하지 않는 트리. 먼저 비교할 값을 정렬한 후(최소 : 오름차순, 최대: 내림차순), 노드를 연결해준다. 이미 공통 부모가 있을 경우 패스하는 방식으로 진행한다. 최종적으로 가지는 간선의 길이는 전체 노드의 갯수 -1

### 이분검색

mid = (lt+rt) / 2

최소값과 최대값을 반씩 나눠서 target number 보다 큰지 작은지 비교해가며 검색하는 방식이다.

[Disjoint-set (서로소 집합)](https://github.com/sosoYim/TIL/blob/main/algorithm/210804-algo-disjoint-union-find.md)

[최소 스패닝 트리(크루스칼, union&find)](https://github.com/sosoYim/TIL/blob/main/algorithm/210804-algo-kruskal.md)

[이분검색](https://github.com/sosoYim/TIL/blob/main/algorithm/210804-algo-dichotomique.md)

## Done

1. 퀴즈 제출 (타임 오버))
2. Algo 예습 (문제 파악)
3. 오늘 배운 것 노션에 정리(이분 검색)
4. TIL

## Todo

- [ ] 코데 3개 풀어가기
- [ ] 모던 자바스크립트 책 구매
- [ ] (포스팅) 후위식 연산 정리
- [ ] (포스팅) 스택프레임, 콜백 함수
- [ ] (포스팅) truty, falsy 정리
- [ ] (포스팅) itterable 한 요소들 정리
- [ ] (포스팅) 순열, 중복순열, 조합 구하기 대표 알고리즘
- [ ] 지난 주 알고리즘 복습(done1,2,3 todo4,5)
- [ ] 인접행렬,인접리스트 정리
- [ ] Bloody fill 정리
- [ ] 드림코딩 앨리 js 4편 보기
- [ ] 크루스칼 코드 구현 정리
- [ ] 이분 검색 코드 구현 정리

### 이 주의 과업

- [ ] 개인 블로그 정리
