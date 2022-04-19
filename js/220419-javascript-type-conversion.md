## javascript 형 변환(Type conversion)
```javascript
// Truthy (true로 인식되는 값)
// true , {}, [], 1, 2, 'false', -12, '3.14' ... 
// 비어있는 객체,배열데이터, 실수, 문자열

// Falsy (false로 인식되는 값)
// false, '', null, undefined, 0, -0, NaN
// 비어있는 문자열, 0

const a = 1
const b = '1'

// 동등연산자 사용 시 형변환이 일어나 true를 반환하므로 
console.log(a == b) // true

// 아래처럼 일치연산자 사용을 권장한다
console.log(a === b) // false
```
