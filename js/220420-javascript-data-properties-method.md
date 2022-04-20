# **js 데이터**

**String**: "", '', ``  
**Number**  
**Boolean**: true, false  
**undefined**  (암시적)  
**null**  (명시적)  
**Array**: []  
**Object**: {}

## **String**
---
```js
const result = 'Hello world!'.indexOf('world')
console.log(result) // 6 (글자 6번째의 w부터 출력하므로 world)

const result = 'Hello world!'.indexOf('Heropy')
console.log(result) // -1 (문자를 찾을수 없을 때 -1 출력)


const str = 'Hello world'
console.log(str.length) // 11 (length: 글자갯수)
console.log(str.indexOf('HEROPY') === -1)  // true
// str 변수의 값에 'HEROPY'가 없으므로 -1 출력, 일치연산자로 -1과 비교하면 true 출력

console.log(str.slice(0, 3)) // Hel
// slice(n,n): n부터 n번째까지 글자 출력

console.log(str.replace('world', 'HEROPY')) //Hello Heropy 
console.log(str.replace(' world', '')) //Hello 
// replace('', ''): 대상 문자열을 변환시킴
// 공백으로 두면 문자가 삭제된다.

console.log(str.trim()) //Helloworld 
// trim(): 모든 공백문자를 제거함

```
## **Number**
---
```js
const pi = 3.14159265358979
console.log(pi) // 3.14159265358979

const str = pi.toFixed(2) //toFixed(): 소숫점 n자리까지 남기고 제거, 문자데이터로 변환된다.
console.log(str) // 3.14
console.log(typeof str) // string

const integer = parseInt(str) // 정수만 추출
const float = parseFloat(str) // 소숫점 포함 추출, 숫자데이터로 변환된다.
console.log(integer) // 3
console.log(float) // 3.14
console.log(typeof integer, typeof float) // number number

console.log(Math.abs(-12)) // 12
// Math.abs(): 숫자의 절대값을 반환

console.log(Math.min(2,8)) // 2
// Math.min(n, n): 숫자의 최소값을 반환

console.log(Math.max(2,8)) // 8
// Math.min(n, n): 숫자의 최대값을 반환

console.log(Math.ceil(3.14)) // 4
// Math.ceil(n.nnn): 숫자를 올림 처리

console.log(Math.floor(3.14)) // 3
// Math.floor(n.nnn): 숫자를 내림 처리

console.log(Math.round(3.14)) // 3
// Math.round(n.nnn): 숫자를 반올림 처리

console.log(Math.random()) // 0.12750402452194365
// Math.random(): 0 이상 1 미만의 부동소숫점 난수 임의로 생성.
function random(){
  return Math.floor(Math.random() * 10)
}
console.log(random()) // 0~9까지의 정수 임의 출력
```

## **Array(배열)**
---
```js
const numbers = [1, 2, 3, 4]
const fruits = ['Apple', 'Banana', 'Cherry']

console.log(numbers[1]) // 2
// 배열(numbers)의 elements(item) [1, 2, 3, 4]의 n번째를 index라 한다. (i로 자주 사용)
// numbers 배열의 zero-base 1번째의 index는 2이다. 
// numbers[0]과 같이 배열의 인덱스를 추출하는 것을 indexing이라 한다.

console.log(fruits[2])  // cheery
console.log(fruits.length) // 3, 배열아이템 갯수 조회
console.log([1, 2].length) // 2, 배열의 literal 부분 직접적으로 출력가능
console.log([].length) // 0, 빈 배열의 아이템 갯수 조회 (배열 데이터 존재유무 식별에 자주 사용)

console.log(numbers.concat(fruits)) // [1, 2, 3, 4, 'Apple', 'Banana', 'Cherry']
// concat(): 원본의 배열데이터에 영향을 끼치지 않고 배열을 병합한다. 

.ForEach() 
// 배열데이터의 element(item)의 갯수만큼 콜백함수(함수의 parameter로 들어가는 함수)를 
// 반복적으로 실행하는 메소드
// fruits배열의 경우 ['Apple', 'Banana', 'Cherry'] item3개 -> 콜백함수 3번 실행

fruits.forEach(function (fruit, i) {
// parameter(매개변수)의 이름은 자유롭게 작명(과일의 단수 fruit 사용)
console.log(fruit, i) // Apple 0  Banana 1  Cherry 2
})

.map()
// forEach와는 다르게 콜백함수 내부의 return 키워드를 통해 반환한 데이터를
// 새로운 배열로 생성해서 사용할 수 있다.

const numbers =  [1, 2, 3, 4]
const fruits = ['Apple', 'Banana', 'Cherry']

//forEach

const a = fruits.forEach(function (fruit, i){
  console.log(`${fruit}-${i}`)
})
console.log(a) //Apple-0 Banana-1 Cherry-2 undefined

// Map
const b = fruits.map(function (fruit, i){
  return `${fruit}-${i}`
})
console.log(b) // ['Apple-0', 'Banana-1', 'Cherry-2']

// Map (Return Object)
const numbers =  [1, 2, 3, 4]
const fruits = ['Apple', 'Banana', 'Cherry']

//forEach

const a = fruits.forEach(function (fruit, i){
  console.log(`${fruit}-${i}`)
})
console.log(a) //Apple-0 Banana-1 Cherry-2 undefined

// Map
const b = fruits.map(function (fruit, i){
  return `${fruit}-${i}`
})
console.log(b) // ['Apple-0', 'Banana-1', 'Cherry-2']

// Map (Return Object)
const b = fruits.map(function (fruit, i){
  return {
    id : i,
    name: fruit
  }
})
console.log(b)
// [{"id": 0, "name": "Apple"}
// {"id": 1,"name": "Banana"}
// {"id": 2, "name": "Cherry"}]

// 위 함수를 화살표 함수로 축약 할 수 있다.
// function 키워드를 지우고 화살표함수 표기 후 return안의 중괄호를 복사
// return을 감싸는 중괄호를 지운 뒤
// 화살표 함수에서 객체데이터를 복사할 것이므로 
// 소괄호안 중괄호({}) 기입한 후 그 안에 객체데이터를 복사해준다.

const b = fruits.map((fruit, i) => ({
  id : i,
  name: fruit
}))
console.log(b) //결과 값은 같다.
```
