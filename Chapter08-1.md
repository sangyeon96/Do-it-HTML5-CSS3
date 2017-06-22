# 08-1 CSS와 박스 모델

### 블록 레벨 요소와 인라인 레벨 요소

#### 블록 레벨\(block-level\) 요소

태그를 사용해 요소를 삽입했을 때 혼자 한 줄을 차지하는 요소. 따라서 그 요소의 왼쪽이나 오른쪽에 다른 요소가 올 수 없다.

ex\) &lt;p&gt;, &lt;h1&gt;~&lt;h6&gt;, &lt;ul&gt;, &lt;ol&gt;, &lt;div&gt;, &lt;blockquote&gt;, &lt;form&gt;, &lt;hr&gt;, &lt;table&gt;, &lt;fieldset&gt;, &lt;address&gt;

#### 인라인 레벨\(inline-level\) 요소

줄을 차지하지 않는 요소. 따라서 한 줄에 여러 개의 인라인 레벨 요소를 표시할 수 있다.

ex\) &lt;img&gt;, &lt;object&gt;, &lt;br&gt;, &lt;sub&gt;, &lt;sup&gt;, &lt;span&gt;, &lt;input&gt;, &lt;textarea&gt;, &lt;label&gt;, &lt;button&gt;

```php
<h3>시간이란..</h3>
<p>내일 죽을 것처럼 오늘을 살고</p>
<p>영원히 살 것처럼 <span>내일을 꿈꾸어라.</span></p>

<!-- 이 예시를 통해 h3, p태그는 블록 레벨, span태그는 인라인 레벨 요소임을 알 수 있다 -->
```

### 박스 모델\(box model\) - 박스 형태의 콘텐츠

블록 레벨 요소들은 모두 박스 형태이다. 예를 들어 &lt;p&gt; 태그를 사용하는 텍스트 단락은 블록 레벨 요소인데 텍스트 단락 앞뒤에 빈 줄이 생기면서 텍스트 단락이 하나의 박스 형태를 가진다. 스타일 시트에서는 이렇게 박스 형태인 요소를 '박스 모델\(box model\) 요소'라고 부른다.![](/assets/box-model.gif)출처 : [http://www.pinsdaddy.com/heres-a-pic-of-the-css-box-model-for-some-strange-reason-everyone-on\_rWzXqUoO0MzbtUo464WCo7WpFtleMxLPTmskwb7eo0PsWRXSsdr0uqt9Y4kLvXp3FGoaiSavB7L7sSg1\*8Z6\|Gv0O65EgwQPujUNx2E0co1h9yczSyRjzGStEEKkne7V/0cdrTDvesP3JViVCD\|sscbS9HQBl5Q\|jJ6fyaGHG4h7elvF6xZaLoJbxcZ2b0Isajej0vPJr9kEhyyRpovHvjjUi3FRd60\|E\*GdFnf40\*Bz9WiHC\*99PdXsuTbXRETdk/](http://www.pinsdaddy.com/heres-a-pic-of-the-css-box-model-for-some-strange-reason-everyone-on_rWzXqUoO0MzbtUo464WCo7WpFtleMxLPTmskwb7eo0PsWRXSsdr0uqt9Y4kLvXp3FGoaiSavB7L7sSg1*8Z6|Gv0O65EgwQPujUNx2E0co1h9yczSyRjzGStEEKkne7V/0cdrTDvesP3JViVCD|sscbS9HQBl5Q|jJ6fyaGHG4h7elvF6xZaLoJbxcZ2b0Isajej0vPJr9kEhyyRpovHvjjUi3FRd60|E*GdFnf40*Bz9WiHC*99PdXsuTbXRETdk/)

박스 모델은 **실제 콘텐츠 영역**, 박스와 콘텐츠 영역 사이의 여백인 **패딩\(padding\)**, 박스의 **테두리\(border\)**, 그리고 여러 박스 모델 사이의 여백인 **마진\(margin\)** 등의 요소로 구성된다. 이 때 마진이나 패딩은 웹 문서에 하나의 콘텐츠만 표시한다면 반드시 필요하지 않을 수도 있지만 다른 콘텐츠들과의 간격이나 배치 등을 고려하면 필요한 박스 모델의 중요한 개념이다.

### width, height 속성 - 콘텐츠 영역의 크기

width 속성은 콘텐츠 영역의 너비, height 속성은 콘텐츠 영역의 높이를 결정한다.

#### 속성 값 종류

* 크기 : px이나 cm
* 백분율 : %
* auto : 자동으로 결정. 기본 값.

#### 실제 콘텐츠 크기 계산하기

여러 요소를 웹 문서에 배치할 때 실제 박스가 차지하는 너비는 width 값에 좌우 패딩 두께와 좌우 테두리 두께를 합쳐 계산한다.

```css
.box{
    width:200px;
    height:auto;
    padding:10px;
    border:5px #ccc solid;
}

/* 박스 모델의 전체 너비
모던 브라우저 = width 값 + 좌우 padding + 좌우 border
인터넷 익스플로러 6 = width 값
(인터넷 익스플로러6의 경우 width값에 패딩과 테두리가 모두 포함된 값이다)
*/
```

### display 속성 - 화면 배치 방법 결정하기

display 속성을 사용하면 블록 레벨 요소를 인라인 레벨 요소로 바꾸거나 인라인 레벨 요소를 블록 레벨 요소로 바꿀 수 있다.

세로로 표시되는 목록\(블록 레벨\)을 가로 내비게이션\(인라인 레벨\)으로 바꿀 때, 한 줄로 표시되는 이미지에 여백과 테두리를 추가해 갤러리로 표시할 때 이 방법을 사용한다.

#### block 속성 값

```css
#block img{
    display:block;
    margin:10px;
}
```

#### inline 속성 값

```css
nav ul li { /* nav는 navigation 요소이다. */
    display:inline;
}
```

#### inline-block 속성 값

요소를 인라인 레벨로 배치하면서 내용에는 블록 레벨 속성을 지정하고 싶다면 이 속성 값을 사용하면 된다.

```css
nav ul li {
    display:inline-block;
    margin:20px;
}
```

#### none 속성 값

이 속성 값을 지정하면 해당 요소를 화면에 아예 표시하지 않는다.

웹 사이트를 반응형 웹 디자인 기법으로 작성할 때 PC용 화면에서는 표시하지만 모바일 화면에서는 보이지 않도록 하고 싶은 부분이 있다면 그 부분을 display:none;으로 처리하면 된다.

#### 기타 display 속성 값들

* inherit
* table : 블록 레벨의 표
* inline-table : 인라인 레벨의 표
* table-row
* table-row-group
* table-header-group
* table-footer-group
* table-column
* table-colum-group
* table-cell
* table-caption
* list-item



