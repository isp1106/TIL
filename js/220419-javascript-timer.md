## javascript 타이머 함수
```javascript
// 타이머함수
// setTimeout(함수, 시간): 일정 시간 후 함수 실행
// setInterval(함수, 시간): 시간 간격마다 함수 실행
// clearTimeout(): 설정된 Timeout 함수를 종료
// clearInterval(): 설정된 Interval 함수를 종료
```

```javascript
setTimeout(function () {
  console.log('Heropy!') // 3초 뒤에 Heropy!
}, 3000)

//Arrow Function
SetTimeout(() => {
  console.log('Heropy!') // 3초 뒤에 Heropy!
}, 3000)

//use variable
const timer = SetTimeout(() => {
  console.log('Heropy!') // 3초 뒤에 Heropy!
}, 3000)

const h1El = document.querySelector('h1')
h1El.addEventListner('click', function () => {
  clearTimeout(timer) // 타이머가 멈춤
})
```

```javascript

//Arrow Function
SetInterval(() => {
  console.log('Heropy!') // 3초 마다 Heropy!
}, 3000)

//use variable
const timer = SetInterval(() => {
  console.log('Heropy!') // 3초 뒤에 Heropy!
}, 3000)

const h1El = document.querySelector('h1')
h1El.addEventListner('click', function () => {
  clearInterval(timer) // 타이머가 멈춤
})
```
