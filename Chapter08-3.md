# 08-3 여백을 조절하는 속성들

### margin 속성 - 요소 주변 여백 설정하기

* margin-top
* margin-right
* margin-bottom
* margin-left
* margin

#### 속성 값

* 크기\(px 또는 cm\)
* 백분율\(%\)
* auto

```css
.margin{
    margin:50px; /* 네 방향 마진 모두 50px */
    margin:30px 50px; /* 위아래 마진-30px, 좌우 마진-50px */
    margin:30px 20px 50px; /* 위 마진-30px, 좌우 마진-20px, 아래 마진-50px */
    margin:30px 50px 30px 50px; /* 위 마진-30px, 우 마진-50px, 아래 마진-30px, 좌 마진-50px */
}
```

### padding 속성 - 콘텐츠 영역과 테두리 사이 여백 설정하기

* padding-top
* padding-right
* padding-bottom
* padding-left
* padding

#### 속성 값

* 크기\(px 또는 cm\)
* 백분율\(%\)
* auto

```css
.padding{
    padding:10px; /* 모든 방향 패딩 10px */
    padding:10px 30px; /* 위아래 패딩-10px, 좌우 패딩-30px */
    padding:10px 30px 10px 30px; /* 위 패딩-10px, 우 패딩-30px, 아래 패딩-10px, 좌 패딩-30px */
}
```



