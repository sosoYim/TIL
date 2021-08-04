# Disjoint-set (서로소 집합)

중복되지 않는 부분집합들에 대한 정보를 저장하고 관리하는 자료구조.

## Union-find

Union-find : Disjoint-set을 위한 대표적인 알고리즘
Union : 노드를 서로소인 집합으로 만들어가는 과정에서 겹치는 부분이 있는 부분집합들을 한 루트에 연결하는 알고리즘
Find: 집합번호를 찾을 때 사용하는 알고리즘

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
