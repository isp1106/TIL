## javascript 상속(확장)
```javascript
class Vehicle {
  constructor(name, wheel) {  //constructor 함수에 name, wheel을 인수로사용, this로 할당
    this.name = name
    this.wheel = wheel
  }
}

const myVehicle = new Vehicle('운송수단', 2)
console.log(myVehicle) // Vehicle {name: '운송수단', wheel: 2}

class Bicycle extends Vehicle {
  constructor(name, wheel, license) {
    super(name, wheel) //super = extends뒤에 있는 vehicle(확장된 클래스)
  }
}

const myBicycle = new Bicycle('삼천리', 2)
const daughtersBicycle = new Bicycle('세발', 3)
console.log(myBicycle) // Bicycle {name: '삼천리', wheel: 2}
console.log(daughtersBicycle) // Bicycle {name: '세발', wheel: 3}

class Car extends Vehicle {
  constructor(name, wheel, license) { //license 인수 추가된 확장
    super(name, wheel)
    this.license = license //this에 license 추가
  }
}
const myCar = new Car('벤츠', 4, true) //license 유무 boolean으로 추가
const daughtersCar = new Car ('포르쉐', 4, false)

console.log(myCar) // Car {name: '벤츠', wheel: 4, license: true}
console.log(daughtersCar) // Car {name: '포르쉐', wheel: 4, license: false}
```
