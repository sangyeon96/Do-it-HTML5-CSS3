# 12-2 속성 선택자

이것도 밑에 코드가 어떻게 생겼는지를 알아두고, 예제파일의 실행결과들을 서로 비교하는게 제일 이해가 잘 된다.

### **\[속성\]** 선택자 - 지정한 속성에 스타일 적용하기

```css
/* <a> 태그 중 href라는 속성이 있는 요소를 찾아내 배경색 지정. */
a[href] {
    background: yellow;
}
```

12/attr1.html 참고.

### **\[속성 = 값\] **선택자 - 특정 값을 갖는 속성에 스타일 적용하기

```css
/* <a> 태그 중 target속성의 값이 _blank인 링크를 찾아 newwindow.png라는 배경 이미지 표시. */
a[target="_blank"] {
    padding-right: 30px;
    background:url(images/newwindow.png) no-repeat center right;
}
```

12/attr2.html 참고.

### **\[속성 ~= 값\]** 선택자 - 여러 값 중 특정 값이 포함된 속성에 스타일 적용하기

이 선택자는 하나의 속성에 속성 값이 여러 개일 때 특정 속성 값을 찾는데 편리하다.

```css
/* class 속성 값에 button이 포함된 요소에 스타일 적용. */
[class ~="button"] {
    border: 2px solid black;
    box-shadow: rgba(0,0,0,0.4) 5px 5px;
}
```

12/attr3.html 참고.

### **\[속성 \|= 값\]** 선택자 - 특정 값이 포함된 속성에 스타일 적용하기

\[속성 ~= 값\]이랑 헷갈릴 수 있지만 \[속성 ~= 값\]은 하이픈\(-\)으로 연결한 단어에 스타일을 적용하지 않는 반면, \[속성 \|= 값\]선택자는 속성 값이 지정한 값이거나 "값-"으로 시작하면 스타일을 적용한다. 다시 말해 **하이픈\(-\)으로 연결한 단어가 있더라도 스타일을 적용한다**.

```css
/* <a> 태그 중 title 속성 값에 us이 포함된 요소에 스타일 적용. us-english같이 하이픈(-)으로 연결한 단어도 적용. */
a[title |="us"] {
    background: url(images/us.png) no-repeat left center;
    padding: 5px 25px;
}

/* <a> 태그 중 title 속성 값에 jp이 포함된 요소에 스타일 적용. */
a[title |="jap"\ {
    background: url(images/jp.png) no-repeat left center;
    padding: 5px 25px;
}
```

12/attr4.html 참고.

### **\[속성 ^= 값\]** 선택자 - 특정 값으로 시작하는 속성에 스타일 적용하기

지정한 문자로 시작하는 속성 값에 대해서만 스타일을 적용한다. 몇 개의 시작글자만 비교해 스타일을 정의한다.

```css
/* <a> 태그 중 title="english"에 스타일 적용 */
a[title ^="eng"] {
    background: url(images/us.png) no-repeat left center;
    padding: 5px 25px;
}

/* <a> 태그 중 title="japanese"에 스타일 적용 */
a[title ^="jap"] {
    background: url(images/jp.png) no-repeat left center;
    padding: 5px 25px;
}

/* <a> 태그 중 title="chinese"에 스타일 적용 */
a[title ^="chin"] {
    background: url(images/ch.png) no-repeat left center;
    padding: 5px 25px;
}
```

12/attr5.html 참고.

### **\[속성 $= 값\]** 선택자 - 특정 값으로 끝나는 속성에 스타일 적용하기

\[속성 ^= 값\] 선택자가 지정한 값으로 시작하는 요소에 스타일을 적용했다면 \[속성 $= 값\] 선택자는 지정한 값으로 끝나는 요소를 찾아 스타일을 적용한다.

```css
/* <a> 태그 중 href="intro.hwp"에 스타일 적용 */
a[href $= "hwp"] {
    background: url(images/hwp_icon.gif) center right no-repeat; /* 배경으로 hwp 아이콘 표시 */
    padding-right: 25px;
}

/* <a> 태그 중 href="intro.xls"에 스타일 적용 */
a[href $= "xls"] {
    background: url(images/excel_icon.gif) center right no-repeat;
    padding-right: 25px;
}
```

12/attr6.html 참고.

### **\[속성 \*= 값\]** 선택자 - 값의 일부가 일치하는 속성에 스타일 적용하기

어느 위치에든 해당 값이 포함되어 있으면 스타일이 적용된다.

```css
/* href 속성 값에 w3라는 값이 포함되면 스타일 적용 */
[href *= "w3"] {
    background:blue;
    color:white;		 
}
```

12/attr7.html 참고.

