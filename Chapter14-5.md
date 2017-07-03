# 14-5 미디어 쿼리를 사용해 사이트 구성하기

### 외부 CSS 파일 연결하기

#### &lt;link&gt; 태그 사용하기

```php
<!-- 기본형 -->
<link rel="stylesheet" media="미디어 쿼리 조건" href="css 파일 경로">

<!-- 예시 -->
<link rel="stylesheet" media="print" href="css/print.css">
<link rel="stylesheet" media="screen and (max-width:768px)" href="css/tablet.css">
```

#### @import 구문 사용하기

```css
@import url("css/tablet.css") only screen and (min-width:321px) and (max-width:768px);
```

### 웹 문서에서 직접 정의하기

첫 번째 방법은 &lt;style&gt; 태그 안에서 media 속성을 사용해 조건을 지정하고 그 조건에 맞는 스타일을 정의하는 것이다.

```php
<!-- 기본형 -->
<style media="미디어 쿼리 조건">
    스타일 규칙들
</style>

<!-- 예시 -->
<style media="screen and (max-width:320px)">
    body {
        background-color: orange;
    }
</style>
```

두 번째 방법은 스타일을 선언할 때 @media 구문을 사용해 각 조건별로 스타일을 지정해 놓고 선택적으로 스타일을 적용하는 것이다.

첫 번째 방법은 하나의 &lt;style&gt; 태그 안에서 하나의 조건을 지정하지만 이 방법은 &lt;style&gt; 태그 안에 여러 조건에 따른 스타일을 모두 나열해 놓고 그 중 선택적으로 스타일을 사용한다.

```php
<!-- 기본형 -->
<style>
    @media 미디어 쿼리 조건{
        스타일 규칙들
    }
</style>

<!-- 예시 -->
<style>
    @media screen and (max-width:320px) {
        body{
            background-color: orange;
        }
    }
</style>
```



