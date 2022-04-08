## 표기법
- dash-case (kebab-case)
- snake_case
- camelCase
- PaselCase
- Zero-based Numbering (특수한 경우를 제외하고 0 부터 번호 매기기)

## 데이터 종류(자료형)
- string
- number
- Boolean
- Undefined
- Null
- Object
- Array

### string (문자 데이터)
```javascript

따옴표를 사용
let myName = 'inseok';
let email = 'dlstjr1106@gmail.com';
let hello = `Hello ${myName}?!`; --> 백틱으로 보간법 사용 `${변수};`

console.log(myName); // HEROPY
console.log(email); // dlstjr1106@gmail.com
console.log(hello); // Hello inseok?!
```
### Number (숫자 데이터)
```javascript
정수 및 부동소수점 숫자

let number = 123;
let opacity = 1.57;

console.log(number); // 123
console.log(opacity); // 1.57 
```
### Boolean (불린 데이터)
```javascript
true, false 두가지 값 밖에 없는 논리 데이터

let checked = true;
let isShow = false;

console.log(checked); // true
console.log(isShow); // false 
```
### undefined
```javascript
값이 할당되지 않은 상태

let undef;
let obj = {abc: 123};

console.log(undef); //  변수에 값 할당x -> undefined 
console.log(obj.abc); // 123
console.log(obj.xyz); // 객체(object)에 없는 value ->  undefined
```
### Null
```
어떤 값이 의도적으로 비어있음을 의미.

let empty = null;

console.log(empty); // null
```

### Object (객체 데이터)
- 여러 데이터를 Key:Value 형태로 저장 {}
```javascript
let user = {
  //  Key: Value,
  
  name: 'INSEOK',
  age: 85,
  isValid:true
};

console.log(user.name); // INSEOK
console.log(user.age); // 85
console.log(user.isValid); // true
```

### Array (배열 데이터)
```javascript
- 여러 데이터를 순차적으로 저장 []
- 제로베이스를 기반으로 출력된다 (0 부터 시작)

let fruit = ['Apple', 'Banana', 'Cherry'];

console.log(fruit[0]); // 'Apple'
console.log(fruit[1]); // 'Banana'
console.log(fruit[2]); // 'Cherry'
```
