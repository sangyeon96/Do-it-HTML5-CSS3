# 04-4 여러 데이터 나열해 보여 주기

### &lt;select&gt;, &lt;optgroup&gt;, &lt;option&gt; 태그 - 드롭다운 목록 만들기

```php
<select 속성="속성 값">
    <option value="값" 속성="속성 값">내용1</option>
    <option value="값" 속성="속성 값">내용2</option>
    <option value="값" 속성="속성 값">내용3</option>
</select>
```

#### &lt;select&gt; 태그의 속성

* **size** : 화면에 표시될 드롭다운 메뉴의 항목 개수를 지정한다.
* **multiple** : 브라우저 화면에 여러 개의 옵션이 함께 표시되면서 Ctrl 키를 누른 상태로 드롭다운 메뉴에 있는 여러 항목을 선택할 수 있다.

#### &lt;option&gt; 태그의 속성

* **value** : 옵션을 선택했을 때 서버로 넘겨질 값을 지정한다.
* **selected** : 화면에 표시될 때 기본으로 선택되어 있는 옵션을 지정한다.

```php
<label class="reg" for="class">학과</label>
<!-- 5개씩 보이고 여러 옵션 선택 가능하다 -->
<select size="5" id="class" multiple>
    <option value="archi">건축공학과</option>
    <option value="mechanic">기계공학과</option>
    <option value="indust">산업공학과</option>
    <option value="elec">전기전자공학과</option>
    <option value="computer" selected>컴퓨터공학과</option>
    <option value="chemical">화학공학과</option>
</select>
```

#### &lt;optgroup&gt; 태그 - 옵션끼리 묶기

```php
<label class="reg" for="class">학과</label>
<select id="class">
    <optgroup label="공과대학">
        <option value="archi">건축공학과</option>
        <option value="mechanic">기계공학과</option>
        <option value="indust">산업공학과</option>
        <option value="elec">전기전자공학과</option>
        <option value="computer" selected>컴퓨터공학과</option>
        <option value="chemical">화학공학과</option>
    </optgroup>
    <optgroup label="인문대학">
        <option value="history">사학과</option>
        <option value="lang">어문학부</option>
        <option value="philo">철학</option>
    </optgroup>
</select>
```

### &lt;datalist&gt; 태그, &lt;option&gt; 태그

&lt;select&gt; 태그 대신 &lt;datalist&gt; 태그를 사용하면 데이터 목록 중에서 값을 선택하도록 만들 수 있다. 즉, 텍스트 필드에 직접 값을 입력하는 것이 아니라 데이터 목록에 제시한 값 중에서 선택하면 그 값이 자동으로 입력된다.

```php
<!-- 기본형 -->
<input type="text" list="데이터 목록 id">
<datalist id="데이터 목록 id">
    <option>내용1</option>
    <option>내용2</option>
    <option>내용3</option>
</datalist>

<!-- 예제 -->
<input type="text" id="interest" list="choices">
<datalist id="choices">
    <option value="grammer" label="문법"></option>
    <option value="voca" label="어휘"></option>
    <option value="speaking" label="회화"></option>
    <option value="listening" label="리스닝"></option>
    <option value="news" label="뉴스청취"></option>
</datalist>
```

### &lt;textarea&gt; 태그 - 여러 줄 입력하는 텍스트 영역 만들기

#### &lt;textarea&gt; 태그의 속성

* **name** : 다른 폼 요소와 구분하기 위해 텍스트 영역의 이름을 지정한다.
* **cols** : 텍스트 영역의 가로 너비를 문자 단위로 지정한다.
* **rows :** 텍스트 영역의 세로 길이를 줄 단위로 지정한다. 지정한 숫자보다 줄 개수가 많아지면 스크롤 막대가 생긴다.

```php
<!-- 기본형 -->
<textarea 속성="속성 값">내용</textarea>

<!-- 예제 -->
<textarea name="intro" cols="60" rows="5">
새로운 일을 시작하는 용기 속에
당신의 천재성과 능력,
그리고 기적이 모두 숨어 있다.

Whatever you can do or dream you can, begin it.
Boldness has genius, power, and magic in it.

요한 볼프강 폰 괴테
Johann Wolfgang von Goethe
</textarea>
```



