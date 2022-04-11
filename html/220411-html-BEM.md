## HTML 클래스 속성의 작명법 (HTML BEM)

- 요소__일부부분 : Underscore(Loadsh) 기호로 요소의 일부분을 표시
```html
- 후손 요소 작명 시 중복 될 수 있는 환경을 방지하고 조금 더 직관적으로 확인 가능

underscore 사용 전
<div class="container">
  <div class="name">
  <div class="item">
    <div class="name"></div>
  </div>
</div>

underscore 사용 후
<div class="container">
  <div class="container__name">
  <div class="item">
    <div class="item__name"></div>
  </div>
</div>
```
- 요소--상태 : Hyphen(dash) 기호로 요소의 상태를 표시

```html
- 관계가 없어보이는 클래스 작명을 방지하고 상태를 직관적으로 확인 가능

Hyphen 사용 전
<div class="btn primary"></div>
<div class="btn sucess"></div>
<div class="btn error"></div>

Hyphen 사용 후
<div class="btn btn--primary"></div>
<div class="btn btn--sucess"></div>
<div class="btn btn--error"></div>
```
