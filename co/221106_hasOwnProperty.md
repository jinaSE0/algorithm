문자열을 입력받아 문자열을 구성하는 각 문자(letter)를 키로 갖는 객체를 리턴해야 합니다.<br>
각 키의 값은 해당 문자가 문자열에서 등장하는 횟수를 의미하는 number 타입의 값이어야 합니다.

내가 푼 코드
```
function countAllCharacters(str) {
  // TODO: 여기에 코드를 작성합니다.
  let obj = {}
   for(let i=0; i<str.length; i++){
     if(obj[str[i]]===undefined){
       obj[str[i]] = 0; 
     } 
     obj[str[i]]++;
   }
   return obj;
}

```

현업 개발자 분이 푼 코드 -> hasOwnProperty와 삼항연산자를 사용함
```
 let obj = {};
  for(let strele of str){
    obj[strele]=obj.hasOwnProperty(strele)?obj[strele]+1:1
    //삼항연산자를 반복문에 쓸 수 있는 이유?
    //값을 평가한 후 할당하기 때문
  }
  return obj
```

**hasOwnProperty** <br>
The hasOwnProperty() method returns a boolean <br>
indicating whether the object has the specified property as its own property (as opposed to inheriting it). <br>
https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Object/hasOwnProperty
