# 14-4 미디어 쿼리

### 미디어 쿼리란?

**미디어 쿼리\(mediaqueri\)**는 CSS3 모듈 중 하나로 사이트에 접속하는 장치에 따라 특정한 CSS 스타일을 사용하도록 해준다.

### 미디어 쿼리 구문

```css
/* 기본형 */
@media [only | not] 미디어 유형 [and 조건] * [and 조건]

/* 예시 */
@media screen and (min-width:200px) and (max-width:360px) {

}
```

#### 연산자

* **and** : 앞의 소스처럼 조건을 계속 추가할 수 있다.
* **,**\(쉼표\) : 동일한 스타일 유형을 사용할 미디어의 유형과 조건이 있다면 쉼표를 이용해 추가한다.
* **only** : 미디어 쿼리를 지원하는 웹 브라우저에서만 조건을 인식하게 한다.
* **not **: not 다음에 지정하는 미디어 유형을 제외한다.

#### 미디어 유형의 종류

* **all** : 모든 미디어 유형
* **print** : 인쇄 장치
* **screen** : 컴퓨터 스크린\(스마트폰 스크린 포함\)
* **tv** : 음성과 영상이 동시 출력되는 TV
* **aural** : 음성 합성 장치\(주로 화면을 읽어 소리로 출력해 주는 장치\)
* **braille** : 점자 표시 장치
* **handheld** : 패드\(pad\)처럼 손에 들고 다니는 장치
* **projection** : 프로젝터
* **tty** : 디스플레이 기능이 제한된 장치\(픽셀\(px\) 단위를 사용할 수 없음\)
* **embossed** : 점자 프린터

### 미디어 쿼리의 조건

미디어 쿼리는 특정 조건에 따라 적용할 CSS를 다르게 정의하므로 조건을 어떻게 체크할 것인지가 중요하다. 미디어 쿼리에서 사용하는 조건에는 주로 화면 크기와 관련된 것들이 많다.

#### 웹 문서의 가로 너비와 세로 높이

##### 속성

* width, height
* min-width, min-height
* max-width, max-height

```css
@media all (min-width:600px) and (max-width:959px) {

}
```

#### 단말기의 가로 너비와 세로 높이

##### 단말기 속성

* device-width, device-height
* min-device-width, min-device-height
* max-device-width, max-device-height

```css
@media all and (min-device-width:320px) and (min-device-height:480px) {

}
```

#### 화면 회전

##### 단말기 속성

* **orientation: portrait** - 단말기 세로 방향
* **orientation: landscape** - 단말기 가로 방향

#### 화면 비율, 단말기의 물리적 화면 비율

##### 속성

* aspect-ratio : 화면 비율\(width값/height값\)
* min-aspect-ratio
* max-aspect-ratio

##### 단말기 속성

* device-aspect-ratio
* min-device-aspect-ratio
* max-device-aspect-ratio

#### 색상당 비트 수

color:1이면 최대 2가지\(2^1\) 색상을 나타낼 수 있고 color:3이면 비트 3개로 표현할 수 있는 최대 색상인 8가지\(2^3\)를 표현할 수 있다.

미디어가 컬러 색상을 지원하지 않는다면 color:0으로 지정한다.

##### 속성 값

* color : 비트 수
* min-color
* max-color

#### 미디어 쿼리 중단점 만들기

미디어 쿼리를 작성할 때 서로 다른 CSS를 적용할 화면 크기를 **중단점\(break point\)**이라고 한다.

