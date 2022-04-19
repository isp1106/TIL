## 호이스팅(Hoisting)
- 함수 선언부가 유호범위(scope) 최상단으로 끌어올려지는 현상
```javascript
const a = 7

double()

const double = function() {
  console.log(a * 2) // double is not function
}
double()
```

```javascript
double()

function double() {
  console.log(a * 2) /// 14
}
```
