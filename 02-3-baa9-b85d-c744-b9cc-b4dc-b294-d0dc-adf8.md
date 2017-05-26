# 02-3 목록을 만드는 태그

### &lt;ul&gt; 태그, &lt;li&gt; 태그 - 순서 없는 목록 만들기

```php
<!-- unordered list-->
<ul>
    <!-- listed item -->
    <li>내용</li>
    <li>내용</li>
    <li>내용</li>
</ul>
```

### &lt;ol&gt; 태그, &lt;i&gt; 태그 - 순서 목록 만들기

#### &lt;ol&gt; 태그 속성

1. type 속성
2. start 속성
3. reversed 속성

```php
<!-- ordered list -->
<ol type="a">
    <!-- listed item -->
    <li>첫 번째 내용</li>
    <li>두 번째 내용</li>
</ol>
<ol type="a" start="3">
    <li>세 번째 내용</li>
</ol>
<ol reversed>
    <li>3위 공개</li>
    <li>2위 공개</li>
    <li>1위 공개</li>
</ol>
```

순서 없는 목록이나 순서 목록 모두 여러 항목이 나열될 때, **&lt;/li&gt; 태그를 생략가능**. \(&lt;li&gt; 태그가 다음에 오는 &lt;li&gt; 태그를 만나면 자동으로 그 전에 &lt;/li&gt; 태그가 있는 것처럼 인식한다.\)

### &lt;dl&gt;, &lt;dt&gt;, &lt;dd&gt; 태그 - 설명 목록 만들기

```php
<!-- description list -->
<dl>
    <!-- description-list term -->
    <dt>제목</dt>
    <!-- description-list description -->
    <dd>설명</dd>
</dl>
```

하나의 &lt;dt&gt; 태그에 여러 개의 &lt;dd&gt; 태그 값을 가질 수도 있고, 여러 개의 &lt;dt&gt; 태그를 가질 수도 있다.

예를 들어 '단어/정의' 목록이나 '질문/답' 목록에서 사용할 수 있다.

HTML 약어 해설을 찾아보다가 흥미로운 사실을 발견하였다. \(출처 : [http://html5doctor.com/the-dl-element/\)](http://html5doctor.com/the-dl-element/)

HTML4에서는 &lt;dl&gt; 태그가 "definition list"로 여겨졌는데, HTML5에서는 "description list"로 변경되었다.

그 이유는 '단어/정의' 목록 뿐만 아니라 '질문/답' 목록 같이 &lt;dt&gt; 태그가 여러 개 이거나, &lt;dd&gt; 태그가 여러 개 일 수 있어서

definition보다는 description이 좀 더 맞는 표현인 것 같다고 생각되어서인 것 같다.\(추측\)

