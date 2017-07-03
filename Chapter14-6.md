# 14-6 플렉서블 박스 레이아웃

### 플렉서블 박스 레이아웃과 새로운 용어

**플렉서블 박스 레이아웃\(flexible box layout\)**이란 그리드 레이아웃을 기본으로 해 플렉스 박스를 원하는 위치에 배치하는 것이다.

### 플렉서블 박스 레이아웃 기본 속성

#### display 속성 - 플렉스 컨테이너 지정하기

##### 속성 값

* **flex** : 플렉스 박스를 박스 레벨 요소로 정의한다.
* **inline-flex** : 플렉스 박스를 인라인 레벨 요소로 정의한다.

#### display 속성과 브라우저 접두사

#### flex-direction 속성 - 플렉스 방향 지정하기

##### 속성 값

* row
* row-inverse
* column
* column-inverse

#### flex-wrap 속성 - 플렉스 항목을 한 줄 또는 여러 줄로 배치하기

##### 속성 값

* **no-wrap** : 플렉스 항목들을 한 줄에 표시한다. 기본 값.
* **wrap** : 플렉스 항목을 여러 줄에 표시한다.
* **wrap-reverse** : 플렉스 항목을 여러 줄에 표시하되 기존 방향과 반대로 배치한다.

#### flex-flow 속성 - 플렉스 방향과 여러 줄의 배치를 한꺼번에 지정하기

##### 속성 값

* 플렉스 방향 : \(flex-direction 속성 값\)
* 플렉스 줄 배치 : \(flex-wrap 속성 값\)

#### flex 속성 - 플렉스 항목 크기 조절하기

##### 속성 값

* &lt;flex-grow&gt;, &lt;flex-shrink&gt;, &lt;flex-basis&gt;
* initial
* auto

### 플렉스 항목 배치를 위한 속성들

속성 값 자세한 설명은 책 참고.

#### justify-content 속성 - 주축 기준의 배치 방법 지정하기

##### 속성 값

* flex-start
* flex-end
* center
* space-between
* space-around

#### align-items 속성, align-self 속성 - 교차축 기준의 배치 방법 지정하기

##### 속성 값

* stretch
* flex-start
* flex-end
* center
* baseline

#### align-content 속성 - 여러 줄일 때의 배치 방법 지정하기

##### justify-content 속성의 속성 값과 같음.





