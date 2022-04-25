## Primitive Type
- `boolean` 
- `number` 
- `string`
- `symbol (ES2015)`
- `null`
- `undefined`

> 오브젝트와 레퍼런스 형태가 아닌 실제 값을 저장하는 자료형
 프리미티브형의 내장 함수를 사용 가능한것은 자바스크립트 처리 방식 덕분
 
 > literal 값으로 Primitive 타입의 서브 타입을 나타낼 수 있다. 
`true`
``` 'hello' ```
`3.14`
`null`
`undefinded`

> - 또는 래퍼 객체로 만들수있다.
```js
new Boolan(fasle) // type of new Boolean(false) : 'object'
new String('world') // type of new Boolean('world') : 'object'
new Number(42) // type of new Boolean(42) : 'object'
```

> TypeScript의 핵심 primitive types 은 모두 소문자.
```js
// ex
function reverse (s: string): string{
  return s.split("").reverse().join("");
}
reverse("hello world")
```

## boolean
```js
let isDone: boolean = false
const isOk: Boolean = true;
isDone = true
console.log(typeof isDone) // 'boolean'
console.log(typeof isOk) // 'boolean'
```

## number
```js
// 모든 숫자는 부동 소수점 값
// 16진수 10진수 외에 ECMA2015에 도입된 2진수 및 8진수를 지원
// NaN
// 1_000_000과 같은 표기 가능 (under_score)
const decimal: number = 6  // 10진수
const hex: number = 0xf00d // 16진수
const binary: number = 0b1010 //2진수
const octal: number = 0o744 //8진수
const notANumber: number = NaN;
const underscoreNum: number = 1_000_000;
```

## String
```js
//Template String
const fullName: string = 'Mark Lee'
const age: number = 39;
const sentence: string = `Hello, My name is ${fullName}.

I'll be ${age + 1} years old next month.`;
console.log(sentence)
//Hello, My name is Mark Lee.
//
//I'll be 40 years old next month.
```

## symbol
```js
// ECMAScript 2015
// new Symbol로 사용할 수 없음
// Symbol을 함수로 사용해서 symbol 타입을 만들어낼 수 있다.
// 프리미티브 타입의 값을 담아서 사용
// 고유하고 수정불가능한 값으로 만들어 줌
// 주로 접근제어에 사용
// 함수를 사용할 때는 대문자 Symbol() , 타입으로 사용할 때는 소문자 symbol을 혼동되지 않게 주의

console.log(Symbol('foo') === Symbol("foo")); // false

const sym = Symbol();
// sym을 이용해서만 객체에서 []를 넣어 접근가능
const obj = {
  [sym]: "value",
}

obj[sym]
```
