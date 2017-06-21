# 07-2 배경 색과 배경 이미지

### background-color 속성 - 배경 색 지정하기

```css
.background-color_notation{
    background-color:#00ff00; /* 16진수 */
    background-color:rgba(0,255,0, 1); /* rgba */
    background-color:green; /* 색상 이름 */
}
```

#### 배경 색 스타일과 상속

예외적으로 background-color 값은 상속되지 않는다.

### background-clip 속성 - 배경 적용 범위 조절하기

* **border-box** : 박스 모델의 가장 외곽인 테두리\(border\)까지 적용한다. 기본 값.
* **padding-box** : 박스 모델에서 테두리를 뺀 패딩\(padding\) 범위까지 적용한다.
* **content-box** : 박스 모델에서 내용 부분에만 적용한다.

### background-image 속성 - 웹 요소에 배경 이미지 넣기

```css
body {background-image: url('bg1.png');}
#area {background-image: url('bg2.png');}
```

### background-repeat 속성 - 배경 이미지 반복 방법 지정하기

* **repeat** : 브라우저 화면에 가득 찰 때까지 배경 이미지를 가로와 세로로 반복한다.
* **repeat-x** : 브라우저 창 너비와 같아질 때까지 배경 이미지를 가로로 반복한다.
* **repeat-y** : 브라우저 창 높이와 같아질 때까지 배경 이미지를 세로로 반복한다.
* **no-repeat** : 배경 이미지를 한 번만 표시하고 반복하지 않는다.

### background-size 속성 - 배경 이미지 크기 조절하기

* **auto** : 원래 배경 이미지 크기만큼 표시된다. 기본 값.
* **contain** : 요소 안에 배경 이미지가 다 들어오도록 이미지를 확대/축소한다.
* **cover** : 배경 이미지로 요소를 모두 덮도록 이미지를 확대/축소한다.
* 크기 값\(px\) : 너비 값과 높이 값을 지정한다. 예시 참고.
* 백분율\(%\) : 배경 이미지가 들어갈 요소의 크기를 기준으로 백분율 값을 지정한다. 예시 참고.

```css
.background-size_notation{
    background-size:auto; /* 원래 배경 이미지 크기 그대로 표시한다. */
    background-size:200px 150px; /* 너비 200px 높이 150px크기로 표시한다. */
    background-size:60% 40%; /* 가로 60% 세로 40%만큼 배경 이미지를 채운다. */
    background-size:contain; /* 요소 안에 모든 배경 이미지가 표시되도록 확대하거나 축소한다. */
    background-size:cover; /* 요소 전체를 모두 덮도록 배경 이미지를 확대하거나 축소한다. */
    background-size:100% 100% /* 요소의 너비와 높이에 맞도록 배경 이미지를 확대하거나 축소한다. */
}
```

### background-position 속성 - 배경 이미지 위치 조절하기

background-position: _수평위치_ _수직위치_;

|  | **키워드 표시법** | **백분율\(%\) 표시법** | **길이\(px\) 표시법** |
| :--- | :--- | :--- | :--- |
| _수평 위치_ | left, center, right | 백분율\(%\) | 길이 값\(px\) |
| _수직 위치_ | top, center, bottom | 백분율\(%\) | 길이 값\(px\) |

```css
.background-position_notation{
    background-position:left top;
    background-position:center;
}
```

### background-origin 속성 - 배경 이미지 배치할 기준 조절하기

* **border-box **: 박스 모델의 가장 외곽인 테두리\(border\)가 기준이 된다.
* **padding-box **: 박스 모델에서 테두리를 뺀 패딩\(padding\)이 기준이 된다. 기본 값.
* **content-box** : 박스 모델에서 내용 부분이 기준이 된다.

### background-attachment 속성 - 배경 이미지 고정하기

* **scroll** : 화면 스크롤과 함께 배경 이미지도 스크롤 된다. 기본 값.
* **fixed** : 화면이 스크롤되더라도 배경 이미지는 고정된다.

### background 속성 - 속성 하나로 배경 이미지 제어하기

```css
/* 예시 */
background:url('images/bg3.jpg') no-repeat fixed right bottom;
/* background-image  background-repeat  background-attachment  background-position  나머지 기본 값 */
```



