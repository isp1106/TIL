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
### DOM API Click Event 예제1
- 빨간 박스 클릭시 console에 Click!! 출력 
```html
- html -
<div class="box"></div>
```
```css
- css -
.box{width:100px; height:100px; background:red;}
```
```javascript
- javascript -
let boxEl = document.querySelector('.box');
console.log(boxEl); 

boxEl.addEventListener('click', function(){
  console.log('Click!!'); /// Click!!
})
///
```

### DOM API Click Event 예제2

```javascript
// HTML 요소(Element) 1개 검색/찾기
const boxEl = document.querySelector('.box');

//요소의 클래스 정보(classList) 객체 활용!
//contains: 포함여부 method
boxEl. classList.add('active');
let isContains = boxEl.classList.contains('active');
console.log(isContains); ///true

boxEl. classList.remove('active');
let isContains = boxEl.classList.contains('active');
console.log(isContains); ///false
```
