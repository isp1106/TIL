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
```
따옴표를 사용

<script>
let myName = 'inseok';
let email = 'dlstjr1106@gmail.com';
let hello = `Hello ${myName}?!`; --> 백틱으로 보간법 사용 `${변수};`

console.log(myName); // HEROPY
console.log(email); // dlstjr1106@gmail.com
console.log(hello); // Hello inseok?!
</script>
```
### Number (숫자 데이터)
```
정수 및 부동소수점 숫자

<script>
let number = 123;
let opacity = 1.57;

console.log(number); // 123
console.log(opacity); // 1.57 
</script>
```
### Boolean (불린 데이터)
```
true, false 두가지 값 밖에 없는 논리 데이터

<script>
let checked = true;
let isShow = false;

console.log(checked); // true
console.log(isShow); // false 
</script>
```
### undefined
```
값이 할당되지 않은 상태

<script>
let undef;
let obj = {abc: 123};

console.log(undef); //  변수에 값 할당x -> undefined 
console.log(obj.abc); // 123
console.log(obj.xyz); // 객체(object)에 없는 value ->  undefined
</script>
```
### Null
```
어떤 값이 의도적으로 비어있음을 의미.

<script>
let empty = null;

console.log(empty); // null
</script>
```

### Object (객체 데이터)
- 여러 데이터를 Key:Value 형태로 저장 {}
```
<script>
let user = {
  //  Key: Value,
  
  name: 'INSEOK',
  age: 85,
  isValid:true
};

console.log(user.name); // INSEOK
console.log(user.age); // 85
console.log(user.isValid); // true
</script>
```

### Array (배열 데이터)
```
- 여러 데이터를 순차적으로 저장 []
- 제로베이스를 기반으로 출력된다 (0 부터 시작)

<script>
let fruit = ['Apple', 'Banana', 'Cherry'];

console.log(fruit[0]); // 'Apple'
console.log(fruit[1]); // 'Banana'
console.log(fruit[2]); // 'Cherry'
</script>
```
