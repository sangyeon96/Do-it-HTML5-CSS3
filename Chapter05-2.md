# 05-2 주요 선택자

### **전체 선택자\(universal selector\)** - 모든 요소에 스타일 적용하기

```css
* {
    font-size: 12px;
    font-family: 돋움;
}
```

### **태그 선택자\(tag selector\)** - 특정 태그를 사용한 요소에 스타일 적용하기

```css
p {
    font-size: 12px;
    font-family: 돋움;
}
h2 {
    font-size: 16px;
    color: blue;
}
```

### **클래스 선택자\(class selector\) **- 특정 부분에 스타일 적용하기

```php
<!doctype html>
<html lang="ko">
    <head>
        <title>클래스 선택자</title>
        <style>
            .intro {
                background-color: yellow;
            }
            .redtext {
                color: red;
            }
        </style>
    </head>
    <body>
        <!-- 요소 전체의 경우 -->
        <h2 class="intro">서론</h2>
        <p class="intro">Hello</p>
        <h2>본론</h2>
        <!-- 일부의 경우 -->
        <p>It's important to show the <span class="redtext">keywords</span></p>
    </body>
</html>
```

### **id 선택자** - 특정 부분에 스타일 적용하기

마침표\(.\) 대신 \(\#\)기호를 사용한다는 점만 제외하면 클래스 선택자와 사용법이 같다. 그런데 클래스 선택자는 문서 안에서 여러 번 반복해 적용할 수 있는 반면, id 선택자는 클래스 선택자와 달리 **문서 안에서 한 번만 적용**할 수 있다.

```php
<!doctype html>
<html lang="ko">
    <head>
        <title>id 선택자</title>
        <style>
            #container {
                background: #ff6a00;
                width: 400px;
                height: 200px;
                margin:0 auto;
            }
        </style>
    </head>
    <body>
        <div id="container"></div>
    </body>
</html>
```

### **그룹 선택자** - 둘 이상 요소에 같은 스타일 적용하기

```css
h1, h2 {
    text-align: center;
}
```



