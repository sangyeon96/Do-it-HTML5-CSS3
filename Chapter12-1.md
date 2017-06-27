# 12-1 연결 선택자\(combination selector\)

이 모든 combination selector들이 영어로 설명이 잘 되어있으니 참고하기 : [http://www.corelangs.com/css/basics/ad-selectors.html](http://www.corelangs.com/css/basics/ad-selectors.html)

밑에 코드가 어떻게 생겼는지를 알아두고, 예제파일의 실행결과들을 서로 비교하는게 제일 이해가 잘 된다.

### **하위 선택자** - 지정한 모든 하위 요소에 스타일 적용하기

descendant selector.

```css
/* 상위요소 하위요소 */
section p { color: blue; }
/* section 요소 안에 있는 모든 p 요소의 글자 색을 파란색으로 지정한다. */
```

12/descendant.html 참고.

### **자식 선택자** - 자식 요소에만 스타일 적용하기

child selector.

```css
/* 부모요소 > 자식요소 */
section > p { color: blue; }
/* section 요소 안에 포함된 p요소 중 자식 p 요소에만 글자 색을 파란색으로 지정한다.(손자 요소는 적용하지 않는다.) */
```

12/child.html 참고.

### **인접 형제 선택자** - 가장 가까운 형제 요소에 스타일 적용하기

adjacent selector.

```css
/* 요소1 + 요소2 */
h1 + p { text-decoration: underline; }
/* h1 요소 다음에 오는 p요소들 중 첫 번째 p 요소에만 밑줄을 긋는다. */
```

12/adjacent.html 참고.

### **형제 선택자** - 형제 요소에 스타일 적용하기

sibling selector.

```css
/* 요소1 ~ 요소2 */
h1 ~ p { text-decoration: underline; }
/* h1 요소 다음에 오는 모든 형제 p 요소에 밑줄을 긋는다. */
```



