# 210803-algo-BFS.md

## **최단거리, 최소 횟수 → BFS를 이용한 레벨탐색**

1. BFS 함수에서 생성하는 변수
   - ch=[] : 탐색할 길이 만큼의 체크 배열 생성하고 0담기
   - queue=[] : 작업판으로 큐 생성
   - L = 0 : 레벨에 0 (해당 레벨의 값이 최단 거리 값이 된다.)
2. BFS 함수의 초기 세팅
   - 생성한 큐에 0레벨의 값 s를 push (루트 노드의 역할)
   - 체크의 s 위치에 1로 체크(한번 다녀간 곳은 체크하지 않음)
3. while 반복문
   - 큐의 길이가 0이 될때까지
     - for문으로 `i=0` 부터 `i<queue.length` 까지 (한 레벨의 모든 노드(부모))
       - 부모 뽑기 `let x = queue.shift();`
         - for문으로 자식 뽑아서 큐에 `push()`
           - 큐에 push한 자식을 ch 배열에 체크(1로 값 바꾸기)
     - L ++ (한 레벨의 모든 노드에 각각의 자식들을 다 뽑아서 큐에 넣었다면 다음 레벨로)

```jsx
//레벨 탐색 : 방법 외우기!!!
//시작점을 루트로 둔 후 갈 수 있는 모든 경우의 수를 2레벨, 이후 계쏙 자식 레벨 생성

function solution(s, e) {
  let answer = 0;

  function BFS() {
    let ch = Array.from({ length: 10001 }, () => 0);
    let queue = [];
    let L = 0; //레벨
    queue.push(s); //0레벨의 값 넣음
    ch[s] = 1;
    while (queue.length) {
      let len = queue.length;
      for (let i = 0; i < len; i++) {
        //레벨별로 돈다. 0: i=1 // 1: i=3; // 2: 27 ...
        let x = queue.shift(); //부모 뽑기
        for (let nx of [x - 1, x + 1, x + 5]) {
          //자식 만들기(문제의 조건)
          if (nx > 0 && nx <= 1000 && ch[nx] === 0) {
            ch[nx] = 1;
            queue.push(nx);
          }
        }
      }
      //레벨 하나에 대한 탐색이 끝나면 길이를 올려준다.
      L++;
    }
  }
  answer = BFS();
  return answer;
}

console.log(solution(5, 14));
```
