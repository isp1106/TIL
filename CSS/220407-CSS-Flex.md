## CSS Flex

```css
[Flex Container]

- display : Flex Container의 화면 출력 특성
		   - flex : 블록 요소와 같이 Flex Container 정의
           - inline-flex : 인라인 요소와 같이 Flex Container 정의

- flex-direction : 주 축을 설정 (행:수평정렬, 열:수직정렬)
			 - row (default) : 행 축 (좌->우)
             - row-reverse : 행 축(우->좌)
             - column : 열 축(위->아래)
             - column-reverse : 열 축(아래->위)

- flex-wrap : Flex Items 묶음(줄 바꿈) 여부
			 - nowrap (default): 묶음(줄 바꿈) 없음
             - wrap : 여러 줄로 묶음
             - wrap-reverse : wrap의 반대 방향으로 묶음

- flex-flow : flex-direction + flex-wrap 합쳐 놓은 약식 속성
			 - ex) flex-flow: row(direction) wrap(wrap);
             
- justyfy-content : 주(수평) 축의 정렬 방법
				   - flex-start (default) : Flex Items를 시작점으로 정렬
                   - flex-end : Flex Items를 끝점으로 정렬
                   - center : Flex Items를 가운데 정렬
                   - space-between : 각 Flex Item 사이를 균등하게 정렬
                   - space-around : 각 Flex Item 외부여백을 균등하게 정렬
                   
- align-content : 교차(수직) 축의 여러 줄 정렬 방법
				   - stretch (default): Flex Items를 시작점으로 정렬
                   - flex-start : Flex Items를 시작점으로 정렬
                   - flex-end : Flex Items를 끝점으로 정렬
                   - center : Flex Items를 가운데 정렬
                   - space-between : 각 Flex Item 사이를 균등하게 정렬
                   - space-around : 각 Flex Item 외부여백을 균등하게 정렬
                   
- align-items : 교차(수직) 축의 한 줄 정렬 방법
				   - stretch (default): Flex Items를 교차 축으로 늘림
                   - flex-start : Flex Items를 각 줄의 시작점으로 정렬
                   - flex-end : Flex Items를 각 줄의 끝점으로 정렬
                   - center : Flex Items를 각 줄의 가운데 정렬
                   - base-line : Flex Items를 각 줄의 문자 기준선에 정렬

[Flex-items]

- order : Flex item의 순서
		- 0 (default): 순서없음
        - 숫자 : 숫자가 작을 수록 먼저
        ex) order: -1; order: 2; -> order: -1; 부터 정렬
        
- flex-grow : Flex item의 증가 너비 비율
		    - 0 (default) : 순서없음
            - 숫자 : 증가 비율
            ex) flex-grow: 1; A:B:C -> 0:1:0 
            
- flex-shrink : Flex item의 감소 너비 비율
			  - 1 (default) : Flex Container 너비에 따라 감소 비율 적용
              - 숫자 : 감소 비율
              - ex) flex-shirink: 0; -> 요소가 줄어들 때 찌그러지지 않음
              
- flex-basis : Flex item의 공간 배분 전 기본 너비
			 - auto (default) : 요소의 content 너비
             - 단위 : px, em, rem 등으로 단위 지정
             - ex) flex-basis: 0; -> 요소의 가로너비를 여백없이 비율 그대로 출력
             
- algin-self : Flex item의 교차 축 아이템 따로 정렬
			 - auto (default) : Flex Container의 align-items 속성의 값을 상속받음
             - stretch/flex-start/flex-end/center/baseline
             - ex) .item:nth-child(1) {align-self: center;}
             	   .item:nth-child(2) {align-self: flex-end;}
```
