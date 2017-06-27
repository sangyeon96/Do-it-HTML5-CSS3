# 11-2 오디오 & 비디오 재생하기

### **&lt;audio&gt;** 태그 - 오디오 파일 삽입하기

#### 속성

* **autoplay** : 오디오를 자동 재생한다.
* **controls** : 웹 화면에 컨트롤 막대를 표시한다. 컨트롤 막대에는 재생/멈춤, 진행 바, 볼륨 등이 표시된다.
* **loop** : 오디오를 반복 재생한다.
* **muted** : 오디오를 재생해 진행하지만 소리는 끈다.
* **preload** : 재생 버튼을 눌러 재생하기 전에 오디오 파일을 다운로드해 준비해 둔다.

```php
<!-- 플레이어와 함께 재생되는 오디오 -->
<audio src="medias/bgsound.mp3" controls></audio>

<!-- 플레이어 없이 재생되는 오디오 -->
<audio src="medias/bgsound.mp3" autoplay loop></audio>
```

### **&lt;video&gt;** 태그 - 비디오 파일 삽입하기

```php
<video src="media/Painting.mp4" controls></video>
```

### **&lt;source&gt;** 태그 - 여러 미디어 파일 한꺼번에 지정하기

#### 속성

* **src** : 미디어 파일의 경로를 지정한다.
* **type **: 웹 브라우저가 해당 미디어 파일을 재생할 수 있는지 여부를 확인할 수 있도록 미디어 파일의 유형을 알려 준다.
* **codecs** : 비디오 코덱을 지정한다.

간단히 type 속성만 사용할 수도 있고 codecs 속성을 이용해 코덱까지 함께 표시할 수도 있다.

```php
<source src="video.ogv" type="video/ogg; codecs='theora,vorbis'">
```

### 이전 브라우저에서는 어떻게 해야 할까?

&lt;video&gt; 태그는 HTML5를 지원하는 브라우저에서만 사용할 수 있기 때문에 모든 사용자들이 비디오를 볼 수는 없다.

```php
<video controls>
    <source src="media/Painting.mp4" type="video/mp4">
    <source src="media/Painting.webm" type="video/webm">
    <source src="media/Painting.ogv" type="video/ogg">
    <!-- 플래시 무비로 변환한 후 플러그인으로 삽입 -->
    <object data="media/Painting.swf" type="application/x-shockwave-flash"></object>
</video>
```

### &lt;audio&gt; 태그와 &lt;video&gt; 태그의 속성

1. **width, heigh**t 속성 - 비디오 크기 조절
2. **controls** 속성 - 컨트롤 막대 표시
3. **preload** 속성 - 파일 다운로드 여부
   * none : 사용자가 재생 버튼을 눌러야만 다운로드하기 시작한다.
   * metadata : 미디어 파일을 즉시 사용하지 않을 것이라고 생각해 미디어 파일 전체를 다운로드하지 않고 메타 정보만 다운로드한다.
   * auto : 사용자가 즉시 이용할 수 있도록 웹 문서를 로드할 때 미디어 파일도 모두 다운로드한다. 다만, 다운로드가 끝나도 사용자가 재생 버튼을 눌러야만 재생된다. 기본 값.
4. **muted** 속성 - 소리는 끄고 화면만 재생
5. **autoplay** 속성 - 자동 재생
6. **loop** 속성 - 반복 재생
7. **poster** 속성 - 문제 상황 표시\(포스터 이미지 대신 표시\)

```php
<video width="400" height="250" controls autoplay muted preload poster="fireworks.jpg">
    <source src="media/Painting.mp4" type="video/mp4">
    <source src="media/Painting.webm" type="video/webm">
    <source src="media/Painting.ogv" type="video/ogg">
    <track src="media/Painting.vtt" srclang="ko" label="Korean" default>
</video>
```

### **&lt;track&gt;** 태그 - 비디오 화면에 자막 추가하기

#### 속성

1. **kind** 속성 - 자막의 종류를 지정한다.
   * subtitles : 자막\(비디오 화면 표시o\)
   * captions : 캡션\(비디오 화면 표시o\)
   * descriptions : 설명\(비디오 화면 표시x\)
   * chapters : 장 제목\(비디오 화면 표시x\)
   * metadata : 콘텐츠 정보\(비디오 화면 표시x\)
2. **src** 속성 - 자막 텍스트의 파일 경로를 지정한다.
3. **srclang** 속성 - 사용한 언어를 지정한다.
4. **label** 속성 - 자막이 여러 개일 경우, 자막을 식별할 수 있도록 제목을 달아 준다.
5. **default** 속성 - 자막 파일이 여러 개일 경우, 기본으로 사용할 자막을 default로 지정할 수 있다.

```php
<!-- 기본형 -->
<track kind="자막 종류" src="경로" srclang="언어" label="제목" default>

<!-- 예시 -->
<track kind="subtitles" src="Wildlife.vtt" srclang="ko" label="korean" default>
```



