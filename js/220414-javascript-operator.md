## 산술 연산자 (arithmetic operator)
```javascript
console.log(1 + 2) // addition(덧셈) 3
console.log(5 - 7) // subtraction(뺄셈) -2
console.log(3 * 4) // multiplication(곱셈) 12
console.log(10 / 2) // division(나눗셈) 5
console.log(7 % 5) // remainder(나눈 나머지) 2
```

## 할당 연산자 (assignment operator)
```javascript
const a = 2
console.log(a) // 2라는 값을 a에 할당
```
```javascript
let b = 2

b = b + 1
// b = b + 1 // (2 + 1) = 3
```
```javascript
b += b + 1
// b = b + 1 // (2 + 1) = 3
```
```javascript
b -= b - 1
// b = b - 1 // (2 - 1) = 1
```
```javascript
b *= 1
// b = b * 1 // (2 * 1) = 2
```
```javascript
b /= 1
// b = b / 1 // (2 / 1) = 2
```
```javascript
b %= 1
// b = b % 1 // (2 / 1) = 2, remainder = 0
```

## 비교 연산자 (comparison operator)
```javascript
const a = 1
const b = 3

console.log(a === b); // false

function isEqual(x, y) {
  return x === y
}
//console.log(isEqual(x, y);
console.log(isEqual(1, 1)) // true (x = 1, y = 2)
console.log(isEqual(2, '2')) // false (x = 2, y = string)
console.log(a !== b) // true (같지 않은지 확인 시 = 기호 2번만 사용)
console.log(a < b) // true (1 < 3)
console.log(a > b) // false (1 > 3)
console.log(a <= b) // true (a가 b보다 작거나 같다)
console.log(a >= b) // false (a가 b보다 크거나 같다)
```

## 논리 연산자 (logical operator)
```javascript
const a = 1 ===1
const b = 'AB' === 'AB'
const c = true
const d = false

console.log(a) // true
console.log(b) // true
console.log(c) // true
console.log(d) // false

- &&(and:그리고) 연산자
console.log('&&: ', a && b && c) // &&: true
console.log('&&: ', a && b && d) // &&: false (1개라도 false-> false 출력)

- ||(or:또는) 연산자
console.log('||: ', a || d) // ||: true (1개라도 true-> true 출력)

- !(not:부정) 연산자
console.log('!: ', !d) // !: true (반대의 값 출력)
```

## 삼항 연산자 (ternary operator)
```javascript
const a = 1 < 2
// a가 1보다 작음

if (a) {
	console.log('true')
} else {
	consoel.log('false')
}
// true

console.log(a ? 'true' : 'false')
// {a, true, false} 3개의 항. 그 사이 {?, :} 기호
// if문을 간소화
// a가 true면 ( : ) 기호 기준 앞에있는 true 출력
// a가 false면  ( : ) 기호 기준 뒤에있는 fasle 출력
```
