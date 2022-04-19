## javascript IIFE (즉시실행함수)

```javascript
// 즉시실행함수
// IIFE, Immediately-Invoked Function Expression

// 일반
const a = 7
function double() {
  console.log(a * 2)
}
double();

// 즉시실행함수 방법 1 (함수 끝에 소괄호 열고닫기)
(function () {
  console.log(a * 2)
})();

// 즉시실행함수 방법 2 (끝 소괄호 앞쪽에 소괄호 열고닫기(권장))
(function () {
  console.log(a * 2)
}());
```
