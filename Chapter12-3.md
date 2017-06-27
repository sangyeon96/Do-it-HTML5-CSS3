# 12-3 가상 클래스와 가상 요소

### 사용자 동작에 반응하는 가상 클래스\(pseudo class\)

사용자가 웹 요소를 클릭하거나 마우스 커서를 올려놓는 등 특정 동작을 할 때 스타일이 바뀌도록 만들고 싶다면 가상 클래스 선택자를 사용한다.

1.  **:link **가상 클래스 선택자 - 방문하지 않은 링크에 스타일 적용
2. **:visited **가상 클래스 선택자 - 방문한 링크에 스타일 적용
3. **:hover **가상 클래스 선택자 - 웹 요소에 마우스 커서를 올려놓을 때의 스타일 적용
4. **:active **가상 클래스 선택자 - 웹 요소를 활성화했을 때의 스타일 적용
5. **:focus **가상 클래스 선택자 - 웹 요소에 초점이 맞추어졌을 때의 스타일 적용

가상 선택자를 링크와 관련해 사용할 때는 **선택자 순서에 주의**해야 한다. 1~5 순서가 바뀌면 스타일을 정의하더라도 제대로 적용되지 않는다.

```css
/* 링크(a:link)와 방문했던 링크(a:visited)의 스타일 지정 */
.navi a:link, .navi a:visited {
    padding: 10px 5px 5px 35px;
    display: block;
    color:#fff;
    width: 150px;
    text-decoration: none; /* 밑줄 없음 */
}

/* 링크 위에 마우스를 올려놓거나(a:hover) 초점을 맞췄을 때(a:focus)의 스타일 지정 */
.navi a:hover,  .navi a:focus {
    text-shadow:0px 2px 2px #000;
    color:#FC0;
}

/* 링크를 클릭했을 때(a:active)의 스타일 지정 */
.navi a:active {
    color:red;
}
```

12/navi.html 참고.

### UI 요소 상태에 따른 가상 클래스

1. **:enabled** 와 **:disabled **가상 클래스 선택자 - 요소를 사용할 수 있을 때와 없을 때의 스타일 지정
2. **:checked** 가상 클래스 선택자 - 라디오 박스나 체크 박스에서 해당 항목을 선택했을 때의 스타일 지정

12/states.html 참고.

### 구조 가상 클래스

1. **:root **가상 클래스 선택자 - 문서 전체에 적용하기
2. **:nth-child\(n\)**와 **nth-last-child\(n\)** 가상 클래스 선택자 - 자식 요소에 위치에 따라 스타일 적용하기
3. **:nth-of-type\(n\)**, **:nth-last-of-type\(n\)** 가상 클래스 선택자 - 특정 태그 위치에 스타일 적용하기
4. **:first-child**, **:last-child** 가상 클래스 선택자 - 첫 번째, 마지막 요소에 스타일 적용하기
5. **:first-of-type**, **:last-of-type **가상 클래스 선택자 - 형제 관계 요소의 위치에 따라 스타일 적용하기
6. **:only-child**, **:only-of-type** 가상 클래스 선택자 - 하나뿐인 자식 요소에 스타일 적용하기

```css
/* 2번. table 요소 안에서 홀수 번째(2n+1) 자식 요소인 tr 요소에 스타일 적용 */
table tr:nth-child(2n+1) {
    background:lightgray;
    color:black;
}

/* 4번. ul의 자식 요소 중 첫 번째 li에 스타일 적용 */
ul.navi li:first-child {
  border-top-left-radius: 1em;
  border-bottom-left-radius: 1em;
}

/* 4번. ul의 자식 요소 중 마지막 li에 스타일 적용 */
ul.navi li:last-child {
  border-top-right-radius: 1em;
  border-bottom-right-radius: 1em;
}

/* 5번. */
p:first-of-type { color: blue; } /* 레벨이 같은 p 요소들 중 첫 번째 p 요소의 글자 색을 파란색으로 지정 */
p:last-of-type { color: blue; } /* 레벨이 같은 p 요소들 중 마지막 p 요소의 글자 색을 파란색으로 지정 */

/* 6번. */
p:only-child { color: green; } /* 자식 요소가 오직 p 요소뿐일 때(다른 자식 요소x) 글자 색을 녹색으로 지정 */
p:only-of-type { font-weight: bold; } /* p 요소가 오직 하나뿐일 때(다른 자식 요소 있어도 됨) p 요소의 글자를 진하게 지정 */
```

12/nth.html, 12/rounded-navi.html 참고.

### 그 외 가상 클래스

1. **:target** 가상 클래스 선택자 - 앵커\(anchor\) 목적지에 스타일 적용하기
2. **:not** 가상 클래스 선택자 - 특정 요소가 아닐 때 스타일 적용하기

```css
/* 1번. 앵커 이름이 #intro인 곳으로 링크하게 될 경우 #intro의 배경 색을 노란색으로 지정*/
#intro:target { background-color: yellow; }

/* 2번. #ex가 아닌 모든 p 요소에서의 글자 색을 파란색으로 지정 */
p:not(#ex) { color: blue; }
```

### 가상 요소

1. **::first-line** 요소와 **::first-letter** 요소 - 첫 번째 줄, 첫 번째 글자에 스타일 적용하기
2. **::before**, **::after **요소 - 내용의 앞뒤에 콘텐츠 추가하기



