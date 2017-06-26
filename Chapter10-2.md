# 10-2 문서 구조를 위한 HTML5 시맨틱 태그

![](/assets/semantic_tag.png)

출처 : [http://www.cellbiol.com/bioinformatics\_web\_development/chapter-3-your-first-web-page-learning-html-and-css/introducing-html5-footer-header-nav-article-section-and-aside-elements/](http://www.cellbiol.com/bioinformatics_web_development/chapter-3-your-first-web-page-learning-html-and-css/introducing-html5-footer-header-nav-article-section-and-aside-elements/)

### **&lt;header&gt;** 태그 - 머리말 지정하기

주로 &lt;form&gt; 태그를 사용해 검색 창을 넣거나 &lt;nav&gt; 태그를 사용해 사이트 메뉴를 넣는다.

### **&lt;nav&gt;** 태그 - 문서를 연결하는 내비게이션 링크

내비게이션 역할을 하는 &lt;nav&gt; 태그는 동일한 사이트 안의 문서나 다른 사이트의 문서로 연결하는 링크 모음을 나타낸다. 이 태그를 사용하면 어느 부분이 내비게이션인지 쉽게 알 수 있다.

&lt;nav&gt; 태그는 내비게이션 메뉴뿐만 아니라 푸터에 있는 사이트 링크 모음 부분에도 많이 사용된다. 다시 말해 사용하는 위치의 영향을 받지 않아 &lt;header&gt;나 &lt;footer&gt; 태그 또는 &lt;aside&gt; 태그 안에 포함시킬 수도 있고 독립해 사용할 수도 있다.

### **&lt;section&gt;** 태그 - 주제별 콘텐츠 영역 나타내기

&lt;section&gt; 태그는 문서에서 콘텐츠 영역을 나타낸다. 다시 말해 &lt;section&gt; 태그는 문맥 흐름 중에서 콘텐츠를 주제별로 묶을 때 사용하며 그 안에는 섹션 제목을 나타내는 &lt;h1&gt;~&lt;h6&gt; 제목 태그가 함께 사용된다. &lt;section&gt; 태그 안에 또 다른 &lt;section&gt; 태그를 넣을 수도 있다.

### **&lt;article&gt;** 태그 - 콘텐츠 내용 넣기

보통 블로그의 포스트나 웹 사이트의 내용, 사용자가 등록한 코멘트, 독립적인 웹 콘텐츠 항목이 해당된다. 다시 말해 태그를 적용한 부분을 떼어 내 독립적으로 배포하거나 재사용하더라도 완전히 하나의 콘텐츠가 된다면 &lt;article&gt; 태그를 쓰면 된다.

보통 &lt;section&gt; 태그와 &lt;article&gt; 태그를 혼동하기도 하는데 &lt;section&gt; 태그는 문맥 흐름 중에서 콘텐츠를 주제별로 묶을 때 사용한다. &lt;article&gt; 태그 안에 &lt;section&gt; 태그를 넣을 수도 있다.

### **&lt;aside&gt;** 태그 - 본문 이외의 내용 표시하기

사이드바는 필수 요소가 아니므로 광고나 링크 모음 등 문서의 메인 내용에 영향을 미치지 않는 내용들을 넣을 때만 사용한다.

### **&lt;iframe&gt;** 태그 - 외부 문서 삽입하기

#### 속성

* width
* height
* name
* src
* seamless

```php
<div class="content">
    <iframe src="embedded.html" width="95%" height="550"></iframe>
</div>
```

### **&lt;footer&gt;** 태그 - 제작 정보와 저작권 정보 표시하기

일반적으로 웹 문서 끝자락에 들어가는 &lt;footer&gt; 태그안에는 사이트 제작자의 연락처 정보와 저작권 정보를 표시한다.

### **&lt;address&gt;** 태그 - 사이트 제작자 정보, 연락처 정보 나타내기

&lt;address&gt; 태그는 주로 &lt;footer&gt; 태그 안에 사용되는데 웹 페이지 제작자의 이름이나 제작자의 웹 페이지 또는 피드백을 위한 연락처 정보를 넣는 데 사용된다.

```php
<footer>
    <address>
        <p>제주특별자치도 남제주군 성산읍 수산리 000 번지 요안도라 </p>
        <p>yoan##@naver.com</p>
    </address>				
    <p> Copyright ⓒ. All rights reserved.</p>      
</footer>
```

### **&lt;div&gt;** 태그는 언제 사용할까?

HTML5에서는 주로 콘텐츠를 묶어 시각적 효과를 적용할 때 즉 콘텐츠에 CSS를 적용할 때 &lt;div&gt; 태그를 사용한다.

```css
#wrapper{
	width:800px;
	margin: 0 auto;	
}
```

```php
<body>
<div id="wrapper">
  <header>
    <nav>
      <ul>
        <li><a href="#">애완견 종류</a></li>
        <li><a href="#">입양하기</a></li>
        <li><a href="#">건강돌보기</a></li>
        <li><a href="#">더불어살기</a></li>
      </ul>
    </nav>
  </header>
  <section>
    <h2>강아지 용품 준비하기</h2>
    <article class="at1">  
      <h3>강아지 집 </h3>
       <p>강아지가 편히 쉴 수 있는 포근한 집이 필요합니다. 강아지의 집은 강아지가 다 큰 후에도 계속 쓸 수 있는 집으로 구입하세요.집을 구입하실 때는 박음질이 잘 되어 있는지, 세탁이 간편한 제품인지 꼭 확인하시고 고르시는 것이 좋습니다.</p>
    </article>
    <article class="at2"> 
      <h3>강아지 먹이 </h3>
      <p>강아지의 먹이는 꼭 어린 강아지용으로 나와있는 사료를 선택하세요. 강아지들은 사람에 비해 성장속도가 8배정도 빠르답니다. 따라서 강아지에게는 성장속도에 맞는 사료를 급여하셔야 합니다. 사람이 먹는 음식을 먹게 되면 양념과 향신료에 입맛이 익숙해지고, 비만이 될 가능성이 매우 높아집니다. 강아지용 사료는 생후 12개월까지 급여하셔야 합니다.</p>
     </article>
     <article class="at3"> 
      <h3>밥그릇, 물병 </h3>
      <p>밥그릇은 쉽게 넘어지지 않도록 바닥이 넓은 것이 좋습니다.물병은 대롱이 달린 것으로 선택하세요. 밥그릇에 물을 주게 되면 입 주변에 털이 모두 젖기 때문에 비위생적이므로 대롱을 통해서 물을 먹을 수 있는 물병을 마련하시는 것이 좋습니다.</p>
     </article>
     <article class="at4"> 
      <h3>이름표, 목줄</h3> 
      <p>강아지를 잃어버릴 염려가 있으니 산책할 무렵이 되면 이름표를 꼭 목에 걸어주도록 하세요. 그리고 방울이 달린 목걸이를 하고자 하실 때는 신중하셔야 합니다. 움직일 때마다 방울이 딸랑 거리면 신경이 예민한 강아지들에게는 좋지 않은 영향을 끼칠 수 있기 때문입니다.</p>
     </article>
  </section>
  <aside>
  	<img src="images/1.png" alt="">
  	<img src="images/2.png" alt="">
  	<img src="images/3.png" alt="">
  </aside>
  <footer>
    <p>Copyright 2012 funnycom</p>
  </footer>
</div>
</body>
```



