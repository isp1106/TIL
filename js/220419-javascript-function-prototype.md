## javascript 생성자 함수(prototype)

```javascript
// 아래와 같이 같은 로직을 사용한 객체데이터가 있다.

const heropy = {
  firsName: 'Heropy',
  lastName: 'Park',
  getFullName: function () {
    return `${this.firsName} ${this.lastName}`
  }
}
console.log(heropy.getFullName()); // Heropy Park

const amy = {
  firstName: 'Amy',
  lastName: 'Clarke',
  getFullName: function () {
    return `${this.firstName} ${this.lastName}`
  }
}
console.log(amy.getFullName()) // Amy Clarke

const neo = {
  firstName: 'Neo',
  lastName: 'Smith',
  getFullName: function () {
    return `${this.firstName} ${this.lastName}`
  }
}
console.log(neo.getFullName()) // Neo Smith
```

```javascript
// 위에서 사용한 객체데이터를 아래와 같이 클래스를 활용하여 간소화한다.

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

console.log(heropy.getFullName()) // Heropy Park
console.log(amy.getFullName()) // Amy Clarke
console.log(neo.getFullName()) // Neo Smith
```
