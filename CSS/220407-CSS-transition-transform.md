## transition (전환)

- transition : 요소의 전환 (시작과 끝) 효과를 지정하는 단축 속성
			   단축형 필수 포함 속성 : 속성명 지속시간 타이밍함수 대기시간;

- transition-property (속성명)
```
 all : 모든 속성에 적용 
 속성이름 : 전환 효과를 사용할 속성 이름 명시 (width 등)
```
- transition-duration (지속시간)
```
0s : 전환 효과 없음
1s : 1초 동안 전환효과 실행
```
- transition-timing-function (타이밍함수 : easing)
```
ease/linear/ease-in/ease-out/ease-in-out/cubic-bezier(n,n,n,n),steps(n)
```
- transition-delay (대기시간)
```
0s : 대기시간 없음
시간 : 대기시간(s)을 지정
## transform (변환)
```
- 2D 변환 함수
```
- translate(x,y)
- scale
-rotate(degree)
-skew(x,y)
-matrix(n,n,n,n,n)
```
- 3D 변환 함수
```
translateZ(z)
translate3d(x,y,z)
scaleZ(z)
scale3d(x,y,z)
rotateX(x)
rotateY(y)
rotateZ(z)
rotate3d(x,y,z,a)
perspective(n)
matrix3d(n,n,n,n,n,n,n,n,n,n,n,n,n,n,n,n)
```
- backface-visibility
```
hidden/visibility
뒷면 숨김 or 보임
```
