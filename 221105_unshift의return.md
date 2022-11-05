배열과 요소를 입력받아 주어진 요소를 배열의 맨 앞에 추가하고 해당 배열을 리턴해야 합니다.<br>
기존 배열에 주어진 요소가 추가된 형태의 배열을 리턴해야 합니다.

처음에 한 답
```
function addToFront(arr, el) {
  // TODO: 여기에 코드를 작성합니다.
  return arr.unshift(el)
}
```

왜 위와 같이하면 안될까? unshift의 리턴값은 배열의 길이이기때문<br>
따라서 배열을 리턴하려면 아래와 같이 만들어야함

```
function addToFront(arr, el) {
  // TODO: 여기에 코드를 작성합니다.
  arr.unshift(el)
  return arr
}
```
