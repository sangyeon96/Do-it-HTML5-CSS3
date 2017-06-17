# 05-1 스타일과 스타일 시트

### 왜 스타일을 사용할까?

**스타일\(style\)**이란 HTML 문서에서 자주 사용하는 글꼴이나 색상, 정렬, 각 요소들의 배치 방법 등 문서의 겉모습을 결정짓는 내용들을 가리킨다.

1. 웹 문서의 내용과 상관없이 디자인만 바꿀 수 있다. - 같은 내용, 다른 형태 체험 사이트 : [http://www.csszengarden.com](http://www.csszengarden.com)
2. 다양한 기기에 맞게 탄력적으로 바뀌는 문서를 만들 수 있다.

### 스타일 형식, 스타일을 표기하는 방법, 스타일 주석

```css
/* 선택자(selector) */
p {
    /* 스타일 속성: 속성 값 */
    text-align: center;
    font-size: 16px;
    color: blue;
}

h2 {
    font-size:20px;
    color: orange;
}
```

### 스타일과 스타일 시트

웹 문서 안에는 여러 개의 스타일 규칙이 사용되는 경우가 많다. 이런 스타일 규칙들을 한눈에 확인하고 필요할 때마다 수정하기도 쉽도록 한 군데 묶어 놓은 것을 '**스타일 시트**'라고 한다. 스타일 시트는 문서 안에서 사용할 스타일 규칙들을 정의한 '**내부 스타일 시트**'와 별도의 스타일 파일을 만들어 연결해 사용하는 '**외부 스타일 시트**'로 나뉜다.

#### 내부 스타일 시트\(Internal Style Sheet\)

스타일 정보는 웹 문서를 브라우저 화면에 표시하기 전에 결정되어야 하기 때문에 모든 스타일 정보는 &lt;head&gt; 태그와 &lt;/head&gt; 태그 안에서 정의해야 하고 &lt;style&gt; 태그와 &lt;/style&gt; 태그 사이에 작성한다.

```php
<!doctype html>
<html lang="ko">
    <head>
        <meta charset="utf-8">
        <title>내부 스타일 시트</title>
        <style>
            ul {
                color: blue;
                list-style-type: square;
            }
        </style>
    </head>
    <body>
        <ul>
            <li>내용1</li>
            <li>내용2</li>
            <li>내용3</li>
        </ul>
    </body>
</html>
```

#### 외부 스타일 시트\(External Style Sheet\)

사이트를 제작할 때는 여러 웹 문서에서 사용할 스타일을 별도 파일로 저장해 놓고 필요할 때마다 파일에서 가져와 사용하는 것이 일반적이다. 이렇게 따로 저장해 놓은 스타일 정보를 '외부 스타일 시트'라고 하고 '**.css**'라는 파일 확장자를 사용한다.

외부 스타일 시트를 연결할 때는 &lt;style&gt; 태그 없이 **&lt;link&gt; 태그**만 사용해 미리 만들어 놓은 외부 스타일 시트 파일을 연결한다.

```php
<!doctype html>
<html lang="ko">
    <head>
        <meta charset="utf-8">
        <title>외부 스타일 시트</title>
        <link href="style.css" rel="stylesheet" type="text/css">
    </head>
    <body>
        <ul>
            <li>내용1</li>
            <li>내용2</li>
            <li>내용3</li>
        </ul>
    </body>
</html>
```

```css
/* style.css 파일 */
ul {
    color: blue;
    list-style-type: square;
}
```

#### 인라인 스타일\(Inline Style\)

간단한 스타일 정보라면 스타일 시트를 사용하지 않고 스타일을 적용할 대상에 직접 표시한다. 이런 방법을 '인라인 스타일'이라고 한다.

```php
<!doctype html>
<html lang="ko">
    <head>
        <meta charset="utf-8">
        <title>인라인 스타일</title>
    </head>
    <body>
        <ul style="color:blue;list-style-type:square;">
            <li>내용1</li>
            <li>내용2</li>
            <li>내용3</li>
        </ul>
    </body>
</html>
```

#### 내부 스타일 시트, 외부 스타일 시트, 인라인 스타일을 비교해주는 이미지

![](/assets/StyleSheets.gif)

출처 : [http://www.jegsworks.com/lessons/web-2/html/stylesheets.htm](http://www.jegsworks.com/lessons/web-2/html/stylesheets.htm)

