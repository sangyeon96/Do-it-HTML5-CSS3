# 06-4 목록과 링크 스타일

### list-style-type 속성 - 목록의 불릿과 번호 스타일 지정하기

#### 순서 없는 목록에서 불릿 모양 바꾸기, 불릿 없애기

```css
.bullet{
    list-style-type:disc; /* 채운 원 */
    list-style-type:circle; /* 빈 원 */
    list-style-type:square; /* 채운 사각형 */
}
.nobullet{
    list-style-type:none; /* 불릿 없애기 */
}
```

#### 순서 목록에서 숫자 바꾸기

```css
.orderedlistnumber{
    list-style-type:decimal; /* 1로 시작하는 십진수 */
    list-style-type:decimal-leading-zero; /* 앞에 0이 붙는 십진수 */
    list-style-type:lower-roman; /* 소문자 로마 숫자 */
    list-style-type:upper-roman; /* 대문자 로마 숫자 */
    list-style-type:lower-alpha; /* 소문자 알파벳 */
    list-style-type:lower-latin;
    list-style-type:upper-alpha; /* 대문자 알파벳 */
    list-style-type:upper-latin;
    list-style-type:armenian; /* 아르메니아 숫자 */
    list-style-type:georgian; /* 조지 왕조시대의 숫자 */
}
```

### list-style-image 속성 - 불릿 대신 이미지 넣기

```css
ul {
    list-style-image:url('images/dot.png');
}
```

### list-style-position 속성 - 목록에 들여 쓰는 효과 내기

* **inside** : 불릿이나 숫자를 안쪽으로 들여 쓴다.
* **outside** : 기본 값으로 불릿이나 숫자를 밖으로 내어 쓴다.

### list-style 속성 - 목록 속성 한꺼번에 표시하기

font 속성과 비슷하게 list-style 속성으로 앞에서 설명한 list-style-type과 list-style-position, list-style-image 속성을 한꺼번에 표시할 수 있다.

```css
ul {
    list-style-type:lower-alpha;
    list-style-position:inside;
}
/* 간단히 줄이면 */
ul {
    list-style:lower-alpha, inside;
}
```

### 



