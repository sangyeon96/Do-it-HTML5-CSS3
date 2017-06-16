# 04-3 &lt;input&gt; 태그의 다양한 속성

### autofocus 속성 - 입력 커서 표시하기

```php
<label class="reg" for="uname">이름</label>
<input type="text" id="uname" autofocus required>
```

### placeholder 속성 - 힌트 표시하기

```php
<label class="reg" for="uid">학번</label>
<input type="text" id="uid" placeholder="하이픈없이 입력">
```

### readonly 속성 - 읽기 전용 필드 만들기

```php
<label class="reg" for="subj">영어회화(초급)</label>
<input type="text" id="subj" value="오전 9:00~11:00" readonly>
```

### required 속성 - 필수 필드 지정하기

```php
<label class="reg" for="uname">이름</label>
<input type="text" id="uname" autofocus required>
```

### min, max, step 속성

세 가지 속성 모두 &lt;input&gt; 태그의 유형이 date이거나 datetime, datetime-local, month, week, time, number, range일 경우에만 사용할 수 있다.

```php
<label class="reg" for="group">단체주문</label>
<input type="number" id="group" value="10" min="10" max="100" step="10">
```

### size, minlength, maxlength 속성 - 길이, 최소 길이, 최대 길이 속성

```php
<label>아이디:<input type="text" id="user_id" size="10" minlength="4" maxlength="15"></label>
<small style="color:red;"> 4~15자리 이내의 영문과 숫자</small>
```



