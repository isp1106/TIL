## 조건문
- 조건의 결과(thruthy,falsy)에 따라 다른 코드를 실행하는 구문

- if
```javascript
let isShow = true;
let checked = false;

if (isShow) {
  console.log('Show!'); // Show!
}

if (checked) {
  console.log('Checked!'); // 출력x
}
```
- if , else
```javascript
let isShow = true;

if (isShow) {
  console.log('Show!'); 
} else{
  console.log('Hide?');
}
isShow의 true/false에 따라 Show! or Hide? 출력
```
