# 11-1 웹과 멀티미디어

### 플러그인 프로그램

보통 인터넷에서 음악을 듣거나 온라인 강의를 시청하려고 할 때 특정 프로그램을 설치하라는 메시지가 뜨는데 이 프로그램이 바로 **플러그인 프로그램**이다. 하지만 플러그인 프로그램은 여러 문제점들이 있었고 HTML5 웹 표준이 지정되면서 점점 사라지고 있다.

ex\) 이제 플래시 플레이어를 차단하고 대부분 HTML5 플레이어를 사용한다.

### &lt;object&gt; 태그와 &lt;embed&gt; 태그 - 플러그인 사용하기

웹 브라우저에서 처리할 수 없는 작업을 위해 웹 문서 안에 포함시킨 외부 프로그램 기능을 '**플러그인\(plug-in\)**'이라고 한다.

이런 플러그인은 &lt;object&gt; 태그와 &lt;embed&gt; 태그로 사용한다.

#### &lt;object&gt; 태그 - 외부 파일 삽입하기

&lt;object&gt; 태그는 웹 브라우저에서 직접 재생할 수 없는 자바 애플릿이나 PDF 파일, 플래시 무비 같은 콘텐츠를 웹 문서 안에 포함시키기 위해 사용한다. 또한 다른 HTML문서도 웹 문서에 포함시킬 수 있다.

##### 속성

* **data** : 외부 파일의 경로를 지정한다.
* **type** : 포함시킨 내용의 유형을 지정한다.
* **name** : 다른 요소들과 구분할 수 있는 이름을 지정한다.
* **width**
* **height**

```php
<!-- 기본형 -->
<object data="경로" type="유형" name="이름" width="너비" height="높이"></object>

<!-- 예시 -->
<object data="CalmBay.swf" type="application/x-shockwave-flash" width="450" height="400"></object>
```

#### &lt;embed&gt; 태그 - 외부 파일 삽입하기

&lt;object&gt; 태그와 달리 닫는 태그가 없는 &lt;embed&gt; 태그는 주로 &lt;object&gt; 태그를 지원하지 않는 이전 브라우저에서 사용된다.

```php
<!-- 기본형 -->
<embed src="경로" type="유형" width="너비" height="높이">

<!-- 예시 -->
<embed src="CalmBay.swf" width="450" height="400">
```

### 멀티미디어의 웹 표준화

아직까지 웹 브라우저마다 재생할 수 있는 멀티미디어 파일 종류가 다르기 때문에 어떤 파일 형식이 표준이 될 것인지가 개발자와 사용자들 사이에서 논의되는 중이다. 브라우저별 비디오/오디오 파일 지원 여부는 책 참고.

#### HTML5와 비디오 코덱

원본 비디오를 최대한 압축해 컴퓨터에서 사용할 수 있는 비디오 파일로 변환하는 과정을 **인코딩\(encoding\)**이라고 한다.

반대로 비디오 파일에 저장되어 있는 비디오 정보를 가져와 비디오 플레이어에 보여주는 과정을 **디코딩\(decoding\)**이라고 한다.

예를 들어 우리가 자주 보는 WMV\(Windows Media Video\)라는 코덱은 원본 비디오를 윈도우의 '윈도우 미디어 플레이어'로 볼 수 있도록 변환해준다.

아직 한 가지 코덱으로 통일되지 않아 다음의 세 가지 비디오 코덱이 함께 사용되고 있다.

1. H.264/AVC
2. v8, v9
3. 오그 테오라\(Ogg Theora\)

#### HTML5와 오디오 코덱

1. MPEG-1 AUDIO Layer3
2. Ogg Vorbis

### HTML5 비디오 변환하기


