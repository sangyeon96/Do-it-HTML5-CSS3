# 09-3 표 스타일

### caption-side 속성 - 표 제목 위치 정하기

#### 속성 값

* **top** : 캡션을 표의 윗부분에 표시한다. 기본 값.
* **bottom** : 캡션을 표의 아랫부분에 표시한다.

### border 속성 - 표 테두리 스타일 결정하기

```css
.table1{
    border:1px solid black; /* 실선 */
}
.table1 td{
    border:1px dotted black; /* 점선 */
    padding:10px;
    text-align:center;
}
```

### border-collapse 속성 - 테두리 통합, 분리하기

#### 속성 값

* **collapse** : 테두리를 하나로 합쳐 표시한다.
* **separate** : 테두리를 따로 표시한다. 기본 값.

### border-spacing 속성 - 인접한 셀 테두리 사이 거리 지정하기

#### 속성 값

* 크기\(px\)

### empty-cells 속성 - 빈 셀의 표시 여부 지정하기

#### 속성 값

* **show** : 빈 셀 주위에 테두리를 그려 빈 셀을 표시한다. 기본 값.
* **hide** : 빈 셀에 테두리를 그리지 않고 비워 둔다.

### width, height 속성 - 표 너비와 높이 지정하기

너비나 높이를 특별히 지정하지 않는다면 셀 안의 내용이 표시될 만큼만 표시된다.

특정한 크기로 표시하고 싶다면 다른 웹 요소들의 너비를 지정할 때처럼 width 속성을 이용해 표와 셀의 너비를 지정하면 된다.

### table-layout 속성 - 콘텐츠에 맞게 셀 너비 지정하기

#### 속성 값

* **fixed** : 셀 너비를 고정한다.
* **auto** : 셀 내용에 따라 셀의 너비가 달라진다. 기본 값.

```css
.table1{
    border-collapse:collapse; /* 표 안의 테두리 합침 */
    width:300px;
    tablelayout:fixed; /* 셀 너비 고정 */
    word-break:break-all; /* 셀 너비보다 긴 내용도 셀 안에 표시 */
    height:auto; /* 셀의 줄 바꿈 따라 높이 값 자동 조정 */
}
```

### text-align 속성 - 셀 안에서 수평 정렬하기

#### 속성 값

* left
* right
* center

### vertical-align 속성 - 셀 안에서 수직 정렬하기

* **baseline**
* sub
* super
* **top**
* **middle**
* **bottom**
* text-top
* text-bottom
* 길이 값\(px\)
* 백분율 값\(%\)



