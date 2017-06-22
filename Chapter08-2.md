# 08-2 테두리 관련 속성들

### border-style 속성 - 테두리 스타일 지정하기

* **none** : 테두리가 나타나지 않는다. 기본 값.
* **hidden** : 테두리가 나타나지 않는다. border-collapse:collapse일 경우, 다른 테두리도 표시되지 않는다.
* **dashed** : 테두리를 짧은 선\(직선으로 된 점선\)으로 표시한다.
* **dotted** : 테두리를 점선으로 표시한다.
* **double **: 테두리를 이중선\(겹선\)으로 표시한다.
* **groove** : 테두리를 창에 조각한 것처럼 표시한다.
* **inset** : border-collapse:separate일 경우, 전체 박스 테두리가 창에 박혀 있는 것처럼 표시되고 border-collapse:collapse일 경우, groove와 똑같이 표시된다.
* **ridge** : 테두리를 창에서 튀어나온 것처럼 표시한다.
* **outset** : border-collapse:separate일 경우, 전체 박스 테두리가 창에서 튀어나온 것처럼 표시되고 border-collapse:collapse일 경우, ridge와 똑같이 표시된다.
* **solid** : 테두리를 실선으로 표시한다.

### border-width 속성 - 테두리 두께 지정하기

* border-top-width
* border-right-width
* border-bottom-width
* border-left-width
* border-width

#### 속성 값

* 크기
* thin
* medium
* thick

### border-color 속성 - 테두리 색상 지정하기

* border-top-color
* border-right-color
* border-bottom-color
* border-left-color
* border-color

### border 속성 - 테두리 스타일 묶어 지정하기

```css
border-top:두께 색상 스타일;
border-right:두께 색상 스타일;
border-bottom:두께 색상 스타일;
border-left:두께 색상 스타일;
border:두께 색상 스타일;
```

두께, 색상, 스타일 순서는 상관 없다.

### border-radius 속성 - 박스 모서리 둥글게 만들기

* border-top-left-radius
* border-top-right-radius
* border-bottom-right-radius
* border-bottom-left-radius
* border-radius

#### 속성 값

* 크기\(px또는 em\) : 반지름 크기
* 백분율\(%\) : 반지름 크기를 %로 지정한다.

#### 타원 형태로 둥글게 만들기

```css
border-top-left-radius:가로크기 세로크기
border-top-right-radius:가로크기 세로크기
border-bottom-right-radius:가로크기 세로크기
border-bottom-left-radius:가로크기 세로크기
border-radius:가로크기 세로크기
```

### box-shadow 속성 - 선택한 요소에 그림자 효과 내기

#### 속성 값

* \(필수\) 수평 거리 수직 거리

* \(선택\) 흐림정도 번짐정도 색상 inset

```css
.box1{
    box-shadow:2px -2px 5px 0px black;
}
.box2{
    box-shadow:5px 5px 15px 5px gray;
}
```

### 



