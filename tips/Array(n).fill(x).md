Array(n).fill(x)
---
: Array(n).fill(x)하면 n개가들어있는 값이없는 배열에 x를 넣는 것

- [x만큼 간격이 있는 n개의 숫자](https://school.programmers.co.kr/learn/courses/30/lessons/12954)

위 문제 다른 사람 풀이 보다가 알았는데 
=> Array(n).fill(x)하면 n개가들어있는 값이없는 배열에 x를 넣는 것


이걸 습득해서 아래문제를 풀었음

- [핸드폰번호가리기](https://school.programmers.co.kr/learn/courses/30/lessons/12948)

```
function solution(phone_number) {
    return Array(phone_number.slice(0, -4).length).fill("*").join("") + phone_number.slice(-4)    
}
```

더 간단한 풀이가 있더라고요,,, 아래도 꼭 참고하자고요,,
```
const solution = n => [...n].fill("*",0,n.length-4).join("")
```
