## 변수 (variable)
```javascript
- 데이터를 저장하고 참조(사용)하는 데이터의 이름
- var (사용x) , let, const
```
```javascript
var 를 사용하면 안되는 이유
- 변수 중복선언이 가능하기 떄문.

var a = 123;
console.log(a); /// 123

var a = 567;
console.log(a); /// 567

위 처럼 a가 2번 선언되었음에도 불구하고, 오류는 발생하지 않는다.
방대한 프로젝트를 개발할 시 똑같은 이름의 변수를 몇번이나 사용해도 오류는 발생하지않으니,
로직상의 오류는 빈번해지고 그 오류를 발견하는 데에도 많은 어려움이 있을 수 있다.
이러한 현상은 <호이스팅> 으로 인해 발생한다.

<호이스팅> 이란
해당 변수의 선언부를 스코프 최상단으로 올려버리는 것을 의미한다.
JavaScript의 변수 생성과 초기화의 작업이 분리되어 진행되기 때문에 이러한 현상이 발생한다.
var는 우리가 기존 C나 Java의 Block-scoped가 아니라 Function-scoped이다.
따라서, 코드 전체의 최상단이 아닌 함수 내부의 최상단으로 이동한다.
이로 인해 var는 for문에서 for문이 종료되어도 접근이 가능해지고 전역변수가 남발될 수 있다.

따라서 값이 변할 수 있는 변수는 let을, 상수엔 const를 사용하고 var 사용을 지양한다.
```

###  let
```javascript
- 재사용이 가능

let a = 2;
let b = 5;
console.log(a + b); /// 7
console.log(a - b); /// -3
console.log(a * b); /// 10
console.log(a / b); /// 0.4

- 값(데이터)의 재할당 가능

let a = 12;
console.log(a); // 12

a = 999;
console.log(a); // 999

```
### const
```javascript
- 값(데이터)의 재할당 불가

const a = 12;
console.log(a); /// 12

a = 999;
console.log(a); /// TypeError : Assginment to constant variable 

```
## 예약어 (reserved word)
```javascript
- 특별한 의미를 가지고 있어, 변수나 함수 이름 등으로 사용할 수 없는 단어

let this = 'Hello!'; /// SyntaxError
let if = 'Hello!'; /// SyntaxError
let break = 'Hello!'; /// SyntaxError

```
