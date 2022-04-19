## javascript 콜백(Callback)
```javascript
// 콜백(Callback)
// 함수의 인수로 사용되는 함수
// 특정한 실행위치를 보장해주는 방법으로 활용가능

// 예제 1

// setTimeout(함수, 시간)
function timeout(cb) {
  setTimeout(() => {
    console.log('Heropy!') //3초 뒤 실행
    cb() // 위 코드 실행된 후에 실행
  }, 3000)
}
timeout(() => {
  console.log('Done!')
})
```

```js
// 예제 2
function sum(a, b, cb) {
  setTimeout(function () {
    cb(a + b)
  }, 1000)
}

sum(2, 5, function (res) {
  console.log(res)
})
```

