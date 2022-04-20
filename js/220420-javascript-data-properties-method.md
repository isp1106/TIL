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

## **Array**
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

.forEach() 
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

// map() 
// Return Object
// map() 메서드는 배열 내의 모든 요소 각각에 대하여 주어진 함수를 호출한 결과를 모아
// 새로운 배열을 반환합니다.
const b = fruits.map(function (fruit, i){
  return `${fruit}-${i}`
})
console.log(b) // ['Apple-0', 'Banana-1', 'Cherry-2']

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

.filter()
// filter() 는 주어진 함수의 테스트를 통과하는 모든 요소를 모아 새로운 배열로 반환합니다.
// 아래 동일한 로직에서 map()과 filter()의 차이를 확인

// map()
const numbers = [1, 2, 3, 4]
const fruits = ['Apple', 'Banana', 'Cherry']

const a = numbers.map(number => {
  return number < 3
})
// 위 코드는 하나의 실행문만 반환하고 있으므로 아래의 형태로 축약가능하다.
const a = numbers.map(number => number < 3)
console.log(a) //true true false false 
//3보다 작은 1, 2, 두개가 true 나머지는 false를 출력한다.

// filter()
const b = numbers.filter(number => number < 3)
console.log(b) //[1, 2] 
//3보다 작은 1, 2가 true이므로 1, 2를 출력한다.

.find()  .findIndex()
const numbers = [1, 2, 3, 4]
const fruits = ['Apple', 'Banana', 'Cherry']

.find()
// 조건에 맞는 특정한 아이템을 찾을 때 
const a = fruits.find(fruit => /^B/.test(fruit))
console.log(a) //Banana
// /^B/ 대문자 B로 시작하는 item(Banana)을 추출하기 위한 정규표현식

.findIndex()
// 특정한 아이템이 몇번째에 있는지 찾을 때
const b = fruits.findIndex(fruit => /^B/.test(fruit))
console.log(b) // 1
// B로 시작하는 item Banana는 zero-base 기준 1번째이므로 1출력

.includes()
//인수로 사용되는 특정한 데이터가 배열에 들어있는지 확인할 때
const a = numbers.includes(3)
console.log(a) //true
// numbers 배열에 3이 포함이 되어있으므로 true
const b = fruits.includes('Heropy')
console.log(b) // false
// fruits 배열에 'Heropy'는 없으므로 false

.push() .unshift()
// 배열의 원본이 수정됨 주의!

.push()
// 배열의 맨 끝에 아이템을 삽입해주는 메소드
numbers.push(5)
console.log(numbers) // [1, 2, 3, 4, 5]
// 배열의 맨 끝에 5가 추가됨

.unshift()
// 배열의 맨 앞에 아이템을 삽입해주는 메소드
numbers.unshift(0)
console.log(numbers) // [0, 1, 2, 3, 4]
// 배열의 맨 앞에 0이 추가됨

.reverse()
// 배열을 역순으로 출력
// 배열의 원본이 수정됨 주의!
numbers.reverse() 
fruits.reverse()
console.log(numbers) // [4, 3, 2, 1]
console.log(fruits) // ['Cherry', 'Banana', 'Apple']

.splice(n, n)
// n번째 item부터 n개 지워준다
// 배열item을 추가하는 목적으로도 사용한다.
// 배열의 원본이 수정됨 주의!
numbers.spice(2, 1) // [1, 2, 3, 4]에서 2번째 item 3부터 1개 지움
console.log(numbers) // [1, 2, 4]

numbers.spice(2, 2) // 2번째 item 3부터 2개 지움
console.log(numbers) // [1, 2]

numbers.spice(2, 0) // 2번째 item 3부터 0개 지움 (지울 item 없음)
console.log(numbers) // [1, 2, 3, 4] 

numbers.spice(2, 0, 999) // 2번째 item 3부터 0개를 지우고 999를 생성
console.log(numbers) // [1, 2, 999, 3, 4] 

numbers.spice(2, 1, 999) // 2번째 item 3부터 1개를 지우고 그 자리에 999를 생성
console.log(numbers) // [1, 2, 999, 4]

numbers.fruits(2, 0, 'Orange') // 2번째인 Cherry 앞에 Orange를 생성
console.log(numbers) //  ['Apple', 'Banana', 'Orange', 'Cherry']
```

## **Object**
---
```js
Object.assign(taget, ...sources)
// Object.assign() 메서드는 출처 객체들의 모든 열거 가능한 자체 속성을 복사해
// 대상 객체에 붙여넣습니다. 그 후 대상 객체를 반환합니다.

const userAge = {
  //key: value
  name: 'Heropy',
  age: '85'
}

const userEmail = {
  //key: value
  name: 'Heropy',
  email: 'thesecon@gmail.com'
}

const target = Object.assign(userAge, userEmail) 
// target(대상): userAge, source(출처): userEmail
console.log(target) // {name: 'Heropy', age: '85', email: 'thesecon@gmail.com'}
console.log(userAge) // {name: 'Heropy', age: '85', email: 'thesecon@gmail.com'}
console.log(target === userAge) // true

// {}, [], function은 참조형 데이터이다.
// 메모리상에서 target인 userAge와 변수 target은 같은 곳을 참조하고 있기 때문에
// 일치연산자로 비교를 해도 true를 출력한다.

// 반면,

const a = { k: 123 }
const b = { k: 123 }
console.log(a === b) // false
// a와 b는 같은 로직의 객체이지만 각각 참조하는 변수가 다르므로
// 일치연산자로 비교시 false를 출력한다.

// 새로운 객체데이터를 사용하려면 
const target = Object.assign({}, userAge, userEmail)
// 위 처럼 target객체를 {}로 설정하고 source 객체에 각각의 배열을 넣어주면
// 원본에 영향이 없는 새로운 객체를 생성 할 수 있다.
console.log(target) // {name: 'Heropy', age: '85', email: 'thesecon@gmail.com'}
console.log(userAge) // {name: 'Heropy', age: '85'}
console.log(target === userAge) // false
// target은 더 이상 userAge와 같은 곳을 참조하지 않기 때문에 fasle를 출력한다.

// 하나의 객체데이터를 복사하는 용도로 assgin()을 사용할 수도 있다.
const target = Object.assign({}, userAge)
console.log(target) // {name: 'Heropy', age: '85'}
console.log(target === userAge) // false
// userAge와 같은 객체를 {}로 새로 복사한 것이며, 
// 복사한 배열은 userAge와 같은 곳을 참조하지 않기 때문에 false를 출력한다.

Object.keys()
// 객체의 key값을 반환

const user = {
  // key: value
  name: 'Heropy',
  age: '85',
  email: 'thesecon@gmail.com'
}

const keys = Object.keys(user)
console.log(keys) // ['name', 'age', 'email']
// user 객체의 key값을 반환

// email의 value 추출에는 2가지 표현이 가능
console.log(user.email) // thesecon@gmail.com
console.log(user['email']) // thesecon@gmail.com 

const values = keys.map(key => user[key]) 
//map()으로 배열 item갯수만큼 3번 받기 (콜백함수 3번실행)

console.log(values) // ['Heropy', '85', 'thesecon@gmail.com']
// 값(value)들만 가진 배열데이터를 생성

```
