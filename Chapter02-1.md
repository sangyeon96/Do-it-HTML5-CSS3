# 02-1 텍스트를 덩어리로 묶어 주는 태그

### &lt;hn&gt; 태그 - 제목 표시하기

```php
<h1>heading1</h1>
<h2>heading2</h2>
<h3>heading3</h3>
<h4>heading4</h4>
<h5>heading5</h5>
<h6>heading6</h6>
```

### &lt;p&gt; 태그 - 단락 만들기

```php
<p>paragraph</p>
```

### &lt;br&gt; 태그 - 줄 바꾸기

닫는 태그가 없다.

### &lt;hr&gt; 태그 - 분위기 전환을 위한 수평 줄 넣기

보통 텍스트 단락의 주제가 바뀔 때 분위기 전환용으로 사용한다.

&lt;hr&gt; 태그를 사용하면 기본으로 가로선이 삽입되는데 CSS를 이용해 가로선을 없앨 수 있다.

&lt;br&gt;과 마찬가지로 닫는 태그가 없다.

### &lt;blockquote&gt; 태그 - 인용문 넣기

```php
<blockquote>인용 내용</blockquote>
```

이 때 인용한 문장은 다른 텍스트보다 안으로 들여 써진다.

```php
<blockquote cite="인용 사이트 주소">인용 내용</blockquote>
<!-- 인용한 사이트 주소가 명확할 경우, cite속성을 이용해 인용 사이트 주소를 표시할 수 있다. -->
```

### &lt;pre&gt; 태그 - 입력하는 그대로 화면에 표시하기

소스에 표시한 공백이 브라우저에 그대로 표시된다.

&lt;code&gt;나 &lt;samp&gt;, &lt;kbd&gt; 같은 태그를 사용해 프로그램 소스를 표시할 때도 소스의 형태를 그대로 브라우저 창에 보여주어야 하기 때문에 사용된다.

```php
<pre>
    function savetheLocal(){
        var second = document.getElementById("second");
        var thevalue = second.value;
        localStorage.setItem(1, thevalue);
        gettheLocal();
    }
</pre>
```



