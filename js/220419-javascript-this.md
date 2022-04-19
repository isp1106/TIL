## this
- 일반(Normal) 함수는 호출 위치에 따라 this 정의!
- 화살표(Arrow) 함수는 자신이 선언된 함수 범위에서 this 정의!

```javascript
// this가 setTimeout 함수에서 호출되기 때문에 name을 가져오지 못한다.

const timer = {
  name: 'Heropy!!',
  timeout: function() {
    setTimeout(function () {
      console.log(this.name) // undefined
    }, 2000)
  }
}
timer.timeout()
// 따라서 화살표 함수를 사용해 timeout 함수범위 에서 호출되게 만든 후 
//this가 상수 timer를 기반으로 정의될 수 있도록 한다.
const timer = {
  name: 'Heropy!!',
  timeout: function() {
    setTimeout(() => {
      console.log(this.name) // Heropy!!
    }, 2000)
  }
}
```
