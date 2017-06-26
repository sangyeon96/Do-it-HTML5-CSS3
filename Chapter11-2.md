# 11-2 오디오 & 비디오 재생하기

### **&lt;audio&gt;** 태그 - 오디오 파일 삽입하기

#### 속성

* **autoplay** : 오디오를 자동 재생한다.
* **controls** : 웹 화면에 컨트롤 막대를 표시한다. 컨트롤 막대에는 재생/멈춤, 진행 바, 볼륨 등이 표시된다.
* **loop** : 오디오를 반복 재생한다.
* **muted** : 오디오를 재생해 진행하지만 소리는 끈다.
* **preload** : 재생 버튼을 눌러 재생하기 전에 오디오 파일을 다운로드해 준비해 둔다.

```php
/* 플레이어와 함께 재생되는 오디오 */
<audio src="medias/bgsound.mp3" controls></audio>

/* 플레이어 없이 재생되는 오디오 */
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
    <object data="media/Painting.swf" type="application/x-shockwave-flash"></object>
</video>
```

### &lt;audio&gt; 태그와 &lt;video&gt; 태그의 속성

### **&lt;track&gt;** 태그 - 비디오 화면에 자막 추가하기



