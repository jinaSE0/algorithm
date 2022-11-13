reduce함수로 배열안에 알파벳이 몇 개씩 있는지 확인하기 + 홀수 인덱스에 있는 애들만

```
const alphabets = ['a','a','a','b','b','c','d','d','e']
const counts = alphabets.reduce((acc, current, i) => {
  if (i % 2 === 1) { // 홀수 인덱스일때만 돌아
    if (acc[current]) { 
      acc[current] += 1; //객체안에 [current] 있니? 있으면 누산해
    } else {
      acc[current] = 1;
    }
  }
  return acc;
}, {}); //마지막이 초깃값
```

https://sso-feeling.tistory.com/298
