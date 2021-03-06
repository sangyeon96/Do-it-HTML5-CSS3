# 02-2 텍스트를 한 줄로 표시하는 태그

### &lt;strong&gt; 태그, &lt;b&gt; 태그 - 굵게 표시하기

경고나 주의사항처럼 중요한 내용이어서 강조해야 할 때는 **&lt;strong&gt; 태그**,

태그를 사용하고 문서의 키워드처럼 단순히 굵게 표시할 때는 **&lt;b&gt; 태그**를 사용한다.

보이는 것이 아니라 **의미가 중심**이다. \(보이는 글씨 크기나 굵기는 똑같다\)

&lt;strong&gt; 태그를 사용하면 그 부분이 강조되었다고 화면 낭독기가 알려준다. \(중요도를 더 높이고 싶다면, &lt;strong&gt; 태그를 여러 번 겹쳐 쓸 수 있다.\)

```php
<!-- strong -->
<strong>굵게 해서 의미를 강조할 텍스트</strong>
<!-- bold -->
<b>단순히 굵게 표시할 텍스트</b>
```

### &lt;em&gt; 태그, &lt;i&gt; 태그 - 이탤릭체로 표시하기

문장에서 흐름상 특정 부분을 강조하고 싶을 때는 **&lt;em&gt; 태그**,

마음 속의 생각이나 꿈, 기술적인 용어, 다른 언어의 관용구 등에는 **&lt;i&gt; 태그**를 사용한다.

이것도 &lt;strong&gt; 태그와 &lt;b&gt; 태그의 차이점과 마찬가지로 두 태그를 **중요도**로 구분한다.

```php
<!-- emphasized text -->
<em>이탤릭체로 의미를 강조할 텍스트</em>
<!-- italic -->
<i>단순히 이탤릭체로 표시할 텍스트</i>
```

### &lt;q&gt; 태그 - 인용 내용 표시하기

**&lt;blockquote&gt; 태그**는 **블록 레벨 태그**이기 때문에 인용 내용이 줄이 바뀌어 나타난다.

**&lt;q&gt; 태그**는 **인라인 레벨 태그**이기 때문에 줄바꿈 없이 다른 내용과 함께 &lt;q&gt; 태그 부분에 **따옴표**를 붙여 한 줄로 표시된다.

&lt;blockquote&gt; 태그와 같이 cite속성을 이용해 인용 사이트 주소를 표시할 수 있다.

```php
<p>웹의 창시자인 팀 버너스 리(Tim Berners-Lee)의 <q cite="http://www.w3.org/standards/webdesign/accessibility"> 웹의 힘은 보편성에 있다. 장애에 구애없이 모든 사람이 접근할 수 있는 것이 필수적인 요소이다.</q>라는 말로 웹 접근성을 설명한다.</p>
```

### &lt;mark&gt; 태그 - 형광펜 효과 내기

```php
<mark>형광펜으로 그어 놓은 듯한 효과를 낼 텍스트</mark>
```

### &lt;span&gt; 태그 - 줄바꿈 없이 영역 묶기

Inline Text Container.

```php
<span style="color:blue;">텍스트 단락에서 일부 글자만 서식(여기선 파란색)을 바꿀 텍스트</span>
```

### &lt;ruby&gt; 태그 - 동아시아 글자 표시하기

주로 동아시아 국가들의 글자들에 주석을 함께 표기하기 위한 용도로 사용된다.

주석으로 표시할 내용을 &lt;ruby&gt; 태그 안에 &lt;rt&gt; 태그로 표시한다.

```php
<ruby> 일본어 글자 <rt> 그 글자의 발음 </rt> </ruby>
```

### 기타 텍스트 관련 태그들

#### &lt;abbr&gt;

abbreviation.

약자 표시. title 속성을 함께 사용할 수 있다.

```php
<p><b><abbr title="Internet of Things">IoT</abbr></b>란 각종 사물에 센서와 통신 기능을 내장해 인터넷에 연결하는 기술을 의미한다.</p>
```

#### &lt;cite&gt;

웹 문서나 포스트에서 참고 내용 표시

```php
<p>내가 경험한 가장 흥미진진한 일은 누군가를 만나는 일이다 - 영화, <cite>'비포선셋'</cite> 중
```

#### &lt;code&gt;

컴퓨터 인식을 위한 소스 코드

```php
<pre><code> function savetheLocal(){...}</code></pre>
```

#### &lt;kbd&gt;

keyboard text.

키보드 입력이나 음성 명령 같은 사용자 입력 내용

```php
<p>웹 화면을 다시 불러오려면 <kbd>F5</kbd>키를 누릅니다</p>
```

#### &lt;small&gt;

부가 정보처럼 작게 표시해도 되는 텍스트

```php
<p>가격 : 13,000원 <small>(부가세 별도)</small></p>
```

#### &lt;sub&gt;

subscript. 아래 첨자

```php
<p>물의 화학식은 <b>H<sub>2</sub>0</b>다</p>
```

#### &lt;sup&gt;

superscript. 위 첨자

```php
<p>E = mc<sup>2</sup></p>
```

#### &lt;s&gt;

strikethrough. 취소선

```php
<p><s>34,000원</s><strong>19,000원</strong></p>
```

#### &lt;u&gt;

underline. 밑줄

```php
<p>링크 표시 용도가 아니라 단순히 밑줄을 긋는다면 <u>u 태그</u></p>
```



