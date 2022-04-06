## 기본문법, 주석
```
span {font-size: 50px;}
- 선택자(selector), {속성(css) : 값(value);}
```
## CSS 선언방식

```
[내장방식, 링크방식, 인라인방식, @import방식]

-내장방식 : <style><style>의 내용으로 작성
-인라인방식: 요소의 style속성에 직접 작성 ex)<div style="color:red;"></div>
-import방식 : @import 규칙으로 CSS 문서안에서 또 다른 문서를 가져와 연결
             ex) @import url("./box.css");
```

## CSS 선택자
```
[기본, 복합, 가상 클래스, 가상 요소, 속성]
- 기본 : 전체선택자 (*), 태그선택자 (ex: li, span, div), 클래스 선택자 (ex: .orange)
- 복합 : 일치선택자 (동시만족 ex: span.orange), 자식선택자 (ex: ul > li), 
		하위선택자 (ex: ul li), 인접형태 선택자 (다음 형제요소 ex: ul li+li), 
        일반형제 선택자 (다음형제 모두선택 ex: ul~li)
- 가상 : :hover, :active, :focus, first-child, last-child, nth-child(n), :not
- 가상요소 : ::before, ::after (가상요소 만들어 삽입, content:''; & add css)
- 속성 : ex): <input type="text" value="1234" disabled>
	      [disabled] { color: red;}
	      <span data-fruit-name="apple">사과</span>
	      [data-fruit-name] {color: red;}
             
[선택자 우선순위]
- 인라인 선언 > id선택자(#) > class선택자(.), 태그선택자(div), 전체선택자(*) 
```

## CSS 대표속성
```
- CSS 단위 (px, em, rem, %, vw, vh)
- width/height : 가로/세로 너비 (max/min)
- margin : 외부여백
- padding : 내부여백
- border : 테두리 선
- border-radius : 모서리 둥글게
- box-sizing : 크기 계산 (border-box/content-box)
- overflow : 넘침 제어 (auto/hidden/scroll)
- display : 출력 속성 (block/inline-block/inline/flex/table etc..)
- opacity : 투명도 (1 or 0.n -> 0 생략가능)
- font-family : 글꼴 (font-size(크기)/font-weight(굵기),serif (글꼴계열)
- line-height/letter-spacing : 행간/자간
- background : 배경 (background-color, repeat, attachment, size, position etc..)
- position : 배치 (static/relative/absolute/fixed, top/right/bottom/left)
- z-index : 요소의 쌓임 (숫자가 높을 수록 위에 쌓임)
```

