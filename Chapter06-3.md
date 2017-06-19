# 06-3 문단 스타일

### direction 속성 - 글자 쓰기 방향 지정하기

* **ltr** : left to right. 기본 값.
* **rtl** : right to left

### text-align 속성 - 텍스트 정렬하기

* **start** : 현재 텍스트 줄의 시작 위치에 맞추어 문단 정렬. ex\) ltr 왼쪽 정렬, rtl 오른쪽 정렬
* **end** : 현재 텍스트 줄의 끝 위치에 맞추어 문단 정렬. ex\) ltr 오른쪽 정렬, rtl 왼쪽 정렬
* **left** : 왼쪽 정렬.
* **right** : 오른쪽 정렬.
* **center** : 가운데 정렬.
* **justify** : 양쪽 정렬.
* **match-parent** : 부모 요소에 따라 문단 정렬.

### text-justify 속성 - 정렬 시 공백 조절하기

text-align속성 값이 justify일 경우, 간격을 어떻게 조절해 정렬할 것인지 지정하기 위해 사용하는 것이 text-justify 속성이다.

* **auto** : 웹 브라우저에서 자동으로 지정한다.
* **none** : 정렬하지 않는다.
* **inter-word** : 단어 사이의 공백을 조절해 정렬한다.
* **distribute **: 인접한 글자 사이의 공백을 똑같이 맞추어 정렬한다.

### text-indent 속성 - 텍스트 들여 쓰기

```css
.indent1 {
    text-indent:15px; /* 크기 */
}
.indent2 {
    text-indent:5%; /* 백분율(부모 요소의 너비를 기준으로) */
}
```

### line-height 속성 - 줄 간격 조절하기

줄 간격은 정확한 단위와 함께 크기 값을 직접 지정하거나 글자 크기를 기준으로 숫자\(몇 배수\), 실제 크기, 백분율로 표시한다.

```css
/* 모두 줄 간격 30px를 나타낸다. */
p {
    font-size:15px;
    line-height:30px;
}
p {
    font-size:15px;
    line-height:2.0;
}
p {
    font-size:15px;
    line-height:200%;
}
```

### text-overflow 속성 - 넘치는 텍스트 표기하기

text-overflow 속성은 해당 요소에서 overflow 속성 값이 hidden이거나 scroll, auto이면서 white-space:nowrap 속성을 함께 사용했을 경우에만 적용된다.

* clip : 넘치는 텍스트를 자른다.
* ellipsis : 말 줄임표\(…\)로 잘린 텍스트가 있다고 표시한다.

```css
.content {
      border:1px solid #ccc;  /* 테두리 */
      width:300px;  /* 단락의 너비 */
      white-space:nowrap;  /* 줄바꿈 없음 */
      overflow:hidden;  /* 넘치는 부분 감춤 */
      text-overflow:ellipsis;  /* 말줄임표 */
 }
.content:hover {
      overflow:visible;  /* 넘치는 부분 보여줌*/
}
```



