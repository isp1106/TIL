## DOM API
- Document Object Model(div, span, input etc..), Application Programming Interface
- javascript에서 DOM API를 제어하는 명령들.
```javascript
// HTML 요소(Element) 1개 검색/찾기
const boxEl = document.querySelector('.box');

// HTML 요소에 적용할 수 있는 메소드!
boxEl.addEventListener();

// 인수 (Arguments)를 추가 가능!
boxEl.addEventListener(1, 2);

// 1 - 이벤트 (Event , 상황)
boxEl.addEventListener('click', 2);

// 2 - 핸들러 (Handler, 실행할 함수)
boxEl.addEventListener('click', function () {
  console.log('Click~!');
});

```
### DOM API 예제1
```html
<div class="box"></div>
```
```javascript
let boxEl = document.querySelector('.box');
console.log(boxEl); 

boxEl.addEventListener('click', function(){
  console.log('Click!!'); /// Click!!
})
///
```

### DOM API 예제2

```javascript
// HTML 요소(Element) 1개 검색/찾기
const boxEl = document.querySelector('.box');

//요소의 클래스 정보(classList) 객체 활용!
//contains: 포함여부 method
boxEl.classList.add('active');
let isContains = boxEl.classList.contains('active');
console.log(isContains); ///true

boxEl.classList.remove('active');
let isContains = boxEl.classList.contains('active');
console.log(isContains); ///false
```

### DOM API 예제3
```html
<div class="box"></div>
<div class="box"></div>
<div class="box"></div>
<div class="box"></div>
```
```javascript
// HTML 요소(Element) 모두 검색/찾기
const boxEls = document.querySelectorAll('.box');
console.log(boxEls); //NodeList4 (div.box *4)

// 찾은 요소들 반복해서 함수 실행!
// 익명 함수를 인수로 추가!
boxEls.forEach(function () {});

// 첫 번째 매개변수(boxEl): 반복 중인 요소
// 두 번째 매개변수(boxEl): 반복 중인 번호
boxEls.forEach(function (boxEl, index) {});

// 출력!
boxEls.forEach(function (boxEl, index) {
  boxEl.classList.add(`order-${index + 1}`);
});
console.log(index, boxEl); 
// <div class="box order-1">
// <div class="box order-2">
// <div class="box order-3">
// <div class="box order-4">
```

### DOM API 예제4

```html
<div class="box"></div>
```
```javascript
const boxEl = document.querySelector('.box');

// Getter, 값을 얻는 용도
console.log(boxEl.textContent); // Box!!

// Setter, 값을 지정하는 용도
boxEl.textContent = 'INSEOK?!';
console.log(boxEl.textContent); // INSEOK?!
```
