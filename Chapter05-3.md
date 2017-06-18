# 05-3 캐스캐이딩 스타일 시트\(CSS\)

### 캐스캐이딩\(Cascading\)의 의미

위에서 아래로 흐른다.

스타일 간의 충돌을 막기 위한 방법이 '**위에서 아래로 흐르며 적용되는 방법**'이다.

이 방법에는 다음 두 가지 원칙이 있다.

1. **스타일 우선순위** - 스타일 규칙의 중요도, 적용 범위에 따라 우선순위가 결정되고 그 우선순위에 따라 위에서 아래로 스타일이 적용된다.
2. **스타일 상속** - 태그들의 포함 관계에 따라 부모 요소의 스타일을 자식 요소로, 위에서 아래로 전달한다.

### 스타일 우선순위

#### 얼마나 중요한가 - 중요도\(Importance\)

1. _사용자_ 스타일 시트의 _중요_ 스타일
2. _제작자_ 스타일 시트의 _중요_ 스타일
3. _제작자_ 스타일 시트의 _일반_ 스타일
4. _사용자_ 스타일 시트의 _일반_ 스타일
5. _브라우저_ 스타일 시트의 스타일

6. _사용자_ 스타일 시트가 최우선!

7. _중요_ 스타일 _**!important**_
8. 기본적인 _브라우저_ 스타일 시트

```css
p {
    font-style:italic;
    color:blue;
}
p {
    color:red !important;
}

/* 최종 적용되는 스타일
p {
    font-style:italic;
    color:red;
}
*/
```

#### 얼마나 한정지을 수 있는가 - 명시도\(Specificity\)

1. 인라인 스타일
2. id 스타일\(\#\)
3. 클래스 스타일\(.\)
4. 태그 스타일

```css
h1 {
    color:blue;
}
#habor {
    border:1px solid gray;
    padding:10px;
    color:green;
}
.heading {
    color:red;
}
```

```php
<h1 class="heading" id="habor">과연 어떤 것이 적용될까</h1>

<!-- 최종 적용되는 스타일
#habor {
    border:1px solid gray;
    padding:10px;
    color:green;
}
-->
```

#### 소스에서의 순서\(Source Order\)

소스에서 나중에 온 스타일이 먼저 온 스타일을 덮어쓴다.

```css
p {
    color:darkgreen;
}
p {
    color:blue;
}

/* 최종 적용되는 스타일
p {
    color:blue;
}
*/
```

### 스타일 상속

스타일 시트에서는 자식 요소에서 별도로 스타일을 지정하지 않으면 부모 요소에 있는 스타일 속성들이 자식 요소로 전달되는데 이것을 '**스타일 상속**'이라고 한다.

```php
<!-- ul태그는 li태그의 부모 요소이므로 li 요소에 모두 적용된다 -->
<ul style="color:red">
    <li>내용1</li>
    <li>내용2</li>
    <li>내용3</li>
</ul>
```

다만, 스타일 상속에서 주의할 것은 **스타일의 모든 속성이 부모 요소에서 자식 요소로 상속되는 것은 아니라는 점**이다.

ex\) 자식 요소의 배경 색이나 배경 이미지는 상속되지 않고 기본 값인 '투명'으로 지정된다.

참고 링크 : [https://opentutorials.org/course/45/5](https://opentutorials.org/course/45/5)

