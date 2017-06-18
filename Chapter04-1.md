# 04-1 폼 만들기

### 웹에서 자주 만나는 폼

폼\(form\)과 관련된 대부분의 작업은 정보를 저장하거나 검색, 수정하는 일인데 이런 작업은 모두 데이터베이스를 기반으로 한다. 따라서 텍스트 상자나 버튼 같은 폼의 형태를 만드는 것은 HTML 태그를 이용하고 그 폼에 입력한 사용자 정보를 처리하는 것은 ASP나 PHP, JSP 같은 서버 프로그래밍을 이용한다.

### &lt;form&gt; 태그 - 폼 만들기

```php
<form 속성="속성값">여러 폼 요소</form>
```

#### form 태그의 속성

1. **method** : 사용자가 입력한 내용들을 서버 쪽 프로그램으로 어떻게 넘겨줄지 지정한다.\(i, ii는 속성값\)
   | 속성값 | get | post |
   | :--- | :--- | :--- |
   | 사용 빈도 |  | 대부분 이 방식 사용 |
   | 주소 표시줄에 사용자가 입력한 내용 표시 | o | x |
   | 입력 내용의 길이 제한 | o \(256byte~4096byte\) | x |
2. **name** : 폼의 이름을 지정한다. 한 문서 안에 여러 개의 &lt;form&gt; 태그가 있을 경우, 폼들을 구분하기 위해 사용한다.
3. **action** : &lt;form&gt; 태그 안의 내용들을 처리해 줄 서버 상의 프로그램을 지정한다.
4. **target** : &lt;action&gt; 태그에서 지정한 스크립트 파일을 현재 창이 아닌 다른 위치에 열도록 지정한다.

#### autocomplete 속성 - 자동 완성 기능

```php
<form action="register.php" autocomplete="off">

</form>
```

### &lt;label&gt; 태그 - 폼 요소에 레이블 붙이기

**레이블\(label\)**이란 입력 창 옆에 붙여 놓은 텍스트.

```php
<!-- 기본형1 -->
<label 속성="속성값">레이블<input ...></label>

<!-- 기본형2 -->
<label for="user-id">
    <input id="user-id" 속성="속성값">
</label>

<!-- 기본형3 -->
<label for="user-id"></label>
<input 속성="속성값" id="user-id">
```

#### 라디오 버튼과 체크박스에서 사용하는 &lt;label&gt; 태그

&lt;label&gt; 태그를 이용해 라디오 버튼이나 체크박스에 텍스트를 연결해 놓았다면 텍스트만 터치해도 라디오 버튼이나 체크박스가 선택되어 사용이 훨씬 쉬워진다.

### &lt;fieldset&gt;, &lt;legend&gt; 태그 - 폼 요소 그룹으로 묶기

하나의 폼 안에서 여러 구역을 나누어 표시하려고 할 때 &lt;fieldset&gt;, &lt;legend&gt; 태그를 사용한다.

```php
<fieldset 속성="속성값">
    <legend>개인 정보</legend>
</fieldset>

<fieldset 속성="속성값">
    <legend>로그인 정보</legend>
</fieldset>
```



