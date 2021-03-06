# 03-2 링크 만들기

### &lt;a&gt; 태그, href 속성 - 링크 만들기

#### &lt;a&gt; 태그 안에서 사용할 수 있는 주요 속성

1. **href**\(hypertext reference\) : 링크한 문서나 사이트의 주소를 입력한다.
2. **target** : 링크한 내용이 표시될 위치\(현재 창 또는 새창\)를 지정한다.
3. **download** : 링크한 내용을 보여주는 것이 아니라 다운로드한다.
4. **rel** : 현재 문서와 링크한 문서의 관계를 알려준다.
5. **hreflang** : 링크한 문서의 언어를 지정한다.
6. **type** : 링크한 문서의 파일 유형을 알려준다.

```php
<h1>텍스트 링크 만들기</h1>
    <a href="http://www.easyspub.com">이지스퍼블리싱 홈페이지</a>
<h1>이미지 링크 만들기</h1>
    <a href="http://www.easyspub.com">
        <img src="images/easyspub.jpg">
    </a>
```

#### 텍스트 링크의 밑줄과 글자 색 바꾸기

텍스트 링크는 기본적으로 _밑줄이 있는 파란색\(blue\)_ 글자로 표시된다. 텍스트 링크를 클릭해 링크된 내용을 한 번 살펴보고 나면 텍스트 링크 색은 _보라색\(purple\)_으로 바뀐다. 또한 텍스트 링크를 누르고 있으면 즉 링크를 활성화시키면 글자 색은 _빨간색\(red\)_으로 바뀐다.

바꾸고 싶은 경우, CSS를 이용해 텍스트 링크의 색을 바꾸고 밑줄을 없앨 수 있다.

```css
<style>
    a {
        text-decoration:none; /* 밑줄 없애기 */
        color:black; /* 링크의 색 */
    }
</style>
```

### target 속성 - 새 탭에서 링크 열기

1. **\_blank** : 링크 내용이 새 창이나 새 탭에서 열린다.
2. **\_self** : **target 속성의 기본 값**으로 링크가 있는 화면에서 열린다.
3. **\_parent** : 프레임을 사용했을 때 링크 내용을 부모 프레임에 표시한다.
4. **\_top** : 프레임을 사용했을 때 프레임에서 벗어나 링크 내용을 전체 화면에 표시한다.

### 한 페이지 안에서 점프하는 앵커 만들기

'**앵커\(anchor\)**'라고 불리는 이 기능은 페이지가 긴 웹 문서에서 특정 요소를 클릭하면 그 위치로 한 번에 이동하도록 도와준다.

```php
<태그 id="앵커 이름">텍스트 또는 이미지</태그>
<a href="#앵커 이름">텍스트 또는 이미지</a>

<ul id="menu">
    <li><a href="#content1">메뉴1</a></li> <!-- 내용1로 이동 -->
    <li><a href="#content2">메뉴2</a></li> <!-- 내용2로 이동 -->
</ul>

    <h2 id="content1">내용1</h2>
    <p><a href="#menu">[메뉴로]</a></p> <!-- 메뉴로 이동 -->

    <h2 id="content2">내용2</h2>
    <p><a href="#menu">[메뉴로]</a></p> <!-- 메뉴로 이동 -->
```

### &lt;map&gt; 태그, &lt;area&gt; 태그, usemap 속성 - 이미지 맵 지정하기

한 이미지상에서 클릭 위치에 따라 서로 다른 링크가 열리도록 하는 것을 '**이미지 맵**'이라고 한다.

#### &lt;area&gt; 태그에서 사용할 수 있는 속성

1. **alt** : 대체 텍스트를 지정한다.
2. **coords** : 링크로 사용할 영역을 _시작 좌표\(a, b\)_와 _끝 좌표\(c, d\)_를 이용해 지정한다.
3. **download** : 링크를 클릭했을 때 링크 문서를 다운로드한다.
4. **href** : 링크 문서\(사이트\) 경로를 지정한다.
5. **media** : 링크 문서\(사이트\)를 어떤 미디어에 최적화시킬지 지정한다.
6. **rel** : 현재 문서와 링크 문서 사이의 관계를 지정한다. \(속성 값 : lternate, bookmark, help, license, next, nofollow, noreferer, prefetch, prev, search, tag\)
7. **shape** : 링크로 사용할 영역의 형태를 지정한다. \(속성 값 : default, rect, circle, poly\)
8. **target** : 링크를 표시할 대상을 지정한다. \(속성 값 : \_blank, \_parent, \_self, \_top, 프레임 이름\)
9. **type** : 링크 문서의 미디어 유형을 지정한다.

```php
<map name="fb">
    <area shape="rect" coords="0,0,80,100" href="http://www.facebook.com" alt="페이스북">
</map>
```



