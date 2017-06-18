# 04-2 사용자 입력을 위한 &lt;input&gt; 태그

HTML5에는 새로운 유형들이 많이 추가되었으나 브라우저에 따라 아직 지원되지 않는 유형도 있다.

### &lt;input&gt; 태그 살펴보기

### &lt;input&gt; 태그 - 입력 항목 만들기

```php
<input type="유형" 속성="속성값">
```

#### id 속성 사용하기

여러 번 사용된 폼 요소를 구분하기 위해 사용하는 것이 **id속성**이다. id를 지정해 놓으면 &lt;label&gt; 태그를 이용해 캡션을 붙일 수도 있고 나중에 배울 CSS를 이용해 각 요소마다 다른 형태로 꾸밀 수도 있다.

### type="hidden" - 히든 필드 만들기

히든\(hidden\) 필드는 화면상의 폼에는 보이지 않지만 사용자가 입력을 마치고 폼을 서버로 전송할 때 서버로 함께 전송되는 요소이다. 보통 사용자에게 굳이 보여 줄 필요가 없지만 관리자가 알아야 하는 것을 히든 필드로 입력한다.

```php
<input type="hidden" name="이름" value="서버로 넘길 값">
```

### type="text" - 텍스트 필드 만들기

한 줄짜리 일반 텍스트를 입력하는 필드이다.

```php
<input type="text" 속성="속성값">
```

#### 텍스트 필드에서 사용할 수 있는 속성

1. **name :** 텍스트 필드를 구별할 수 있도록 이름을 붙인다.
2. **size** : 텍스트 필드의 길이를 지정한다.
3. **value** : 텍스트 필드 요소가 화면에 표시될 때 텍스트 필드 부분에 표시될 내용이다.
4. **maxlength **: 텍스트 필드에 입력할 수 있는 최대 문자 개수를 지정한다.

### type="password" - 비밀번호 입력란 만들기

```php
<form>
    <fieldset>
        <label>아이디: <input type="text" id="user-id" size="10"></label>
        <label>비밀번호: <input type="password" id="user-pw" size="10"></label>
        <input type="submit" value="로그인">
    </fieldset>
</form>
```

### type="search", type="url", type="email", type="tel" - 분화된 텍스트 필드

#### type="search" - 검색 상자 만들기

```php
<input type="search">
<input type="submit" value="검색">
```

#### type="url" - URL 입력란 만들기

```php
<input type="url" 속성="속성값">
```

type="url"을 사용했을 때 이 필드에는 반드시 '\[\[[http://'로\]\(http://'로\]\(http://'로\]\(http://'로\)\](http://'로]%28http://'로]%28http://'로]%28http://'로%29\)\) 시작하는 사이트 주소를 입력해야 한다.

#### type="email" - 메일 주소 입력란 만들기

```php
<input type="email" 속성="속성값">
```

#### type="tel" - 전화번호 입력란 만들기

```php
<input type="tel" 속성="속성값">
```

### type="number" - 숫자 입력하기

```php
 <label>주문 개수: <input type="number" min="1" max="5" value="1"></label>
```

브라우저에서 다음 소스를 열었을 때 크롬이나 인터넷 익스플로러 창에서는 일반 텍스트 필드처럼 표시되지만 파이어폭스에서는 스핀 박스로 표시된다.

### type="range" - 슬라이드 막대로 숫자 지정하기

type="range"는 type="number"를 슬라이드 막대를 움직여 값을 입력하게 한다.

```php
<label>주문 개수: <input type="range" min="1" max="5" value="1"></label>
```

#### type="number"필드와 type="range"필드에서 사용할 수 있는 속성

1. **min** : 필드에 입력할 수 있는 최솟값을 지정한다.\(type="range"일 때 기본 최솟값은 0이다\)
2. **max** : 필드에 입력할 수 있는 최댓값을 지정한다.\(type="range"일 때 기본 최댓값은 100이다\)
3. **step** : 짝수나 홀수 등 특정 숫자로 제한하려고 할 때 숫자 간격을 지정할 수 있다.
4. **value** : 필드에 표시할 초기값

### type="radio", type="checkbox" - 라디어 버튼과 체크박스 넣기

radio는 라디오 버튼\(동그라미\), checkbox는 체크박스\(네모\)

```php
<input type="radio" 속성="속성값">
<input type="checkbox" 속성="속성값">
```

#### 라디오 버튼과 체크박스에서 사용할 수 있는 속성

1. **name** : 라디오 버튼이나 체크박스가 여러 개 있을 경우, 서버의 폼 프로그램에서 라디오 버튼이나 체크박스를 구분하기 위해 이름을 지정한다.
2. **value :** 선택한 라디오 버튼이나 체크박스를 서버로 알려 줄 때 넘길 값을 지정한다. 필수 속성이다.
3. **checked** : 라디오 버튼의 항목들을 처음에 아무 것도 선택되지 않은 상태로 화면에 표시되는데 기본으로 선택해 놓을 항목이 있다면 checked 속성을 사용한다.

### type="color" - 색상 선택 상자 표시하기

색상 값은 **16진수**로 표시한다.

```php
<label>선호 색상 <input type="color" value="#00ff00"></label> <!-- 여기서 value는 초록색 -->
```

### type="date", type="month", type="week" - 날짜 표시하기

```php
<!-- yyyy-mm-dd -->
<input type="date">
<!-- yyyy-mm -->
<input type="month">
<!-- yyyy-W몇번째 -->
<input type="week">
```

### type="time", type="datetime", type="datetime-local" - 시간 지정하기

```php
<input type="time">
<input type="datetime">
<input type="datetime-local">
```

#### 날짜나 시간과 관련된 유형을 지정할 때 공통으로 사용하는 속성

1. **min** : 날짜나 시간의 최솟값을 지정한다.
2. **max** : 날짜나 시간의 최댓값을 지정한다.
3. **step** : 스핀 박스의 화살표를 누를 때마다 날짜나 시간을 얼마나 조절할지를 지정한다.
4. **value** : 화면에 표시할 초기값을 지정한다.

### type="submit", type="reset" - 서버 전송, 리셋 버튼 넣기

리셋\(reset\) 버튼은 &lt;input&gt; 요소에 입력된 모든 정보를 재설정해 사용자가 입력한 내용을 모두 지울 수 있다.

submit 버튼으로 전송된 정보는 처음에 &lt;form&gt; 태그에서 지정한 폼 처리 프로그램에 넘겨진다.

```php
<form action="register.php" method="post">
    <label> 메일 주소 <input type="text"></label>
    <input type="submit" value="제출">
    <input type="reset" value="다시입력">
</form>
```

### type="image" - 이미지 버튼 넣기

단순히 이미지 버튼을 넣는 것이 아니라 type="submit"의 기능도 포함되어 있다. submit 버튼 대신 전송 이미지를 넣은 것이다.

```php
<input type="image" id="butt" src="images/login.jpg" alt="login">
```

### type="button" - 버튼 넣기

폼 안에 버튼 형태를 만든다. 이 버튼은 submit이나 reset 같은 자체 기능이 없고 오직 버튼만 넣기 때문에 스크립트 함수 등을 연결해 사용한다.

value 속성을 사용해 버튼에 표시할 내용을 지정한다.

```php
<input type="button" value="버튼 기능" onclick="function()">
```

### type="file" - 파일 첨부하기

type="file" 필드를 넣으면 웹 브라우저 화면에 \[파일 선택\]이나 \[찾아보기\]등이 표시되는데 이 버튼을 클릭한 후 파일을 선택하면 파일이 첨부된다.

```php
<label> 첨부파일 <input type="file"></label>
```



