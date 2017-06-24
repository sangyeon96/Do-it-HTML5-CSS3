# 09-1 CSS 포지셔닝과 주요 속성들

### CSS 포지셔닝이란?

CSS를 이용해 꾸미고 CSS 포지셔닝을 이용해 검색 창, 로그인 창, 광고, 뉴스, 실시간 검색 순위 등 여러 요소를 적절히 배치하면 지금 우리가 보고 있는 형태로 바뀐다.

브라우저 화면 안에 각 콘텐츠 영역을 어떻게 배치할지를 결정하는 것이 지금부터 배울 **float 속성**과 **position 속성**이다.

### box-sizing 속성 - 박스 너비 기준 정하기

#### 속성 값

* **content-box** : width 속성 값을 콘텐츠 영역 너비 값으로 사용한다. 기본 값.
* **border-box** : width 속성 값을 콘텐츠 영역에 테두리까지 포함한 박스 모델 전체 너비 값으로 사용한다.

```css
.box1 { /* 콘텐츠 영역 너비 width 300 + padding 30*2 + border 2*2 = 364px가 실제 화면에서 차지하는 너비 */
	box-sizing:content-box;
	width: 300px;
	height: 150px;
	margin: 10px;
	padding: 30px;
	border:2px solid red;
}
.box2 { /* 화면에서 차지하는 너비는 width 300px, 콘텐츠 영역 너비는 width 300 - padding 30*2 - border 2*2 = 236px */
	box-sizing:border-box;
	width: 300px;
	height: 150px;
	margin: 10px;
	padding: 30px;
	border: 2px solid red;
}
```

### float 속성 - 왼쪽이나 오른쪽으로 배치하기

#### 속성 값

* left
* right
* none

float:left나 float:right를 지정하면 너비 값은 콘텐츠를 표시할 때 필요한 만큼만 차지하고 다른 요소가 들어올 만큼의 공간을 비워 둔다.

### clear 속성 - float 속성 해제하기

float 속성이 더 이상 유용하지 않다고 알려 주는 속성이 clear 속성이다.

#### 속성 값

* none
* left
* right
* both : float 속성 값이 left인지 right인지와 상관없이 무조건 기본 상태로 되돌리고 싶을 때

### position 속성 - 배치 방법 지정하기

position 속성은 웹 문서 안의 요소들을 자유자재로 배치해 주는 속성이다.

position 속성을 이용하면 텍스트나 이미지를 나란히 배치할 수 있고 여러 개의 요소를 가로나 세로로 원하는 위치에 배치할 수도 있다.

#### 속성 값

* static : 요소를 문서의 흐름에 맞추어 배치한다.
* relative : 이전 요소에 자연스럽게 연결해 배치하되 위치를 지정할 수 있다.
* absolute : 원하는 위치를 지정해 배치한다.
* fixed : 지정한 위치에 고정해 배치한다. 화면에서 요소가 잘릴 수도 있다.

### visibility 속성 - 요소를 보이게 하거나 보이지 않게 하기

### z-index 속성 - 요소 쌓는 순서 정하기



