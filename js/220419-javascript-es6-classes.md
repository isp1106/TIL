## ES6 Classes
- 일반함수인 `nomal: function()`을 `normal()`로 축약
```javascript
const heropy = {
  name: 'Heropy',
  normal() {  // 일반함수인 nomal: function()을 normal()로 축약가능
    console.log(this.name)
  },
  arrow: () => {
    console.log(this.name)
  }
}

heropy.normal()
heropy.arrow()
```
- `prototype`으로 작성된 코드를 es6 class를 활용해 축약
```javascript
////prototype (축약 전)

function User(first, last) {
  this.firstName = first
  this.lastName = last
}

User.prototype.getFullName = function () {
  return `${this.firstName} ${this.lastName}`
}

const heropy = new User('Heropy', 'Park') // 생성자 함수 (PascalCase)
const amy = new User('Amy', 'Clarke') // 생성자 함수
const neo = new User('Neo', 'Smith') // 생성자 함수

console.log(heropy) // User {firstName: 'Heropy', lastName: 'Park'}
console.log(amy.getFullName()) // Amy Clarke
console.log(neo.getFullName()) // Neo Smith
```
```javascript
//class (축약 후)

class User { //생성자 함수
  constructor(first, last) { //contstuctor : function()을 //cunstructor()로 생략
    this.firstName = first
    this.lastName = last
  }
  getFullName() {
    return `${this.firstName} ${this.lastName}`
  }
}

const heropy = new User('Heropy', 'Park') // 생성자 함수 (PascalCase)
const amy = new User('Amy', 'Clarke') // 생성자 함수
const neo = new User('Neo', 'Smith') // 생성자 함수

console.log(heropy) // User {firstName: 'Heropy', lastName: 'Park'}
console.log(amy.getFullName()) // Amy Clarke
console.log(neo.getFullName()) // Neo Smith
```
