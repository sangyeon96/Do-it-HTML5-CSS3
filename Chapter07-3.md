# 07-3 그러데이션 효과로 배경 꾸미기

### 그러데이션과 브라우저 접두사

현재의 표준화된 구문이 완성되었지만 아직 웹 상에는 이전 브라우저가 남아 있다. 따라서 현재의 표준화된 구문 외에도 그러데이션을 지원하지 않는 브라우저와 접두사를 붙여 사용하는 브라우저까지 고려해 함께 입력해야 한다.

#### 브라우저 접두사

* **-webkit-** : 사파리 5.1~6.0 \(현재 10\)
* **-moz-** : 파이어폭스 3.6 ~ 15
* **-o-** : 오페라 11.1 ~ 12.0

### 선형 그러데이션\(linear-gradient\)

색상이 수직이나 수평 또는 대각선 방향으로 일정하게 변하는 것. 색상이 어느 방향으로 바뀌고 어떤 색상으로 바뀌는지 알려 주어야 한다.

```css
linear-gradient(각도 to 방향, color-stop, [color-stop,...])
```

#### 방향

* to top
* to left
* to right
* to bottom : 기본 값.

접두사와 함께 선형 그러데이션을 사용할 때는 붙이는 기준이 약간씩 다르므로 구분해 사용해야 한다.

| 접두사\(브라우저\) | 그러데이션 시작 위치 기준 | 그러데이션 끝 위치 기준 | 키워드 to 사용 |
| :--- | :--- | :--- | :--- |
| -webkit-\(사파리\) | o | x | o |
| -moz-\(파이어폭스\) | x | o | x |
| -o-\(오페라\) | x | o | x |

```css
.grad{
    background: blue; /* css3 미지원 브라우저 */
    background: -webkit-linear-gradient(left top, blue, white); /* 초기 사파리(시작 위치, 시작 색상, 끝 색상) */
    background: -moz-linear-gradient(right bottom, blue, white); /* 초기 파이어폭스(끝 위치, 시작 색상, 끝 색상) */
    background: -o-linear-gradient(right bottom, blue, white); /* 초기 오페라(끝 위치, 시작 색상, 끝 색상) */
    background: linear-gradient(to right bottom, blue, white); /* 표준 구문(그러데이션 방향, 시작 색상, 끝 색상) */
}
```

#### 각도

이때의 각도는 그러데이션이 끝나는 각도이고 그 값은 '**deg**'로 표기한다.

CSS에서 각도는 맨 윗부분이 0deg이고 시계 방향으로 회전하면서 90deg, 180deg가 된다.

```css
.grad{
    background: #0000ff; /* css3 미지원 브라우저 */
    background-image: -webkit-linear-gradient(45deg, #0000ff, #ffffff); /* 초기 사파리용(끝부분 각도, 시작 색상, 끝 색상) */
    background-image: -moz-linear-gradient(45deg, #0000ff, #ffffff); /* 초기 파이어폭스용(끝부분 각도, 시작 색상, 끝 색상) */
    background: -o-linear-gradient(45deg, #0000ff, #ffffff); /* 초기 오페라용(끝부분 각도, 시작 색상, 끝 색상) */
    background: linear-gradient(45deg, #0000ff, #ffffff); /* 표준 구문(끝부분 각도, 시작 색상, 끝 색상) */
}
```

#### 색상 중지 점\(color-stop\)

선형 그러데이션을 만들기 위해서는 바뀌는 부분의 색을 지정해 주어야 하는데 바뀌는 지점을 **색상 중지 점\(color-stop\)**이라고 한다.

```css
.grad{
    background: #06f; /* css3 미지원 브라우저 */
    background: -webkit-linear-gradient(top, #06f, white 30%, #06f); /* 초기 사파리용(시작 색상, 중지 점 색상과 위치, 끝 색상) */
    background: -moz-linear-gradient(bottom, #06f, white 30%, #06f); /* 초기 파이어폭스용(시작 색상, 중지 점 색상과 위치, 끝 색상) */
    background: -o-linear-gradient(bottom, #06f, white 30%, #06f); /* 초기 오페라용(시작 색상, 중지 점 색상과 위치, 끝 색상) */
    background: linear-gradient(to bottom, #06f, white 30%, #06f); /* 표준 구문(시작 색상, 중지 점 색상과 위치, 끝 색상) */
}
```

### 원형 그러데이션

```css
radial-gradient(최종모양 크기 at 위치, color-stop, [color-stop,...])
```

#### 모양

원형 그러데이션에서 만들어지는 모양은 circle\(원형\)과 eclipse\(타원형\)이다. 따로 지정하지 않으면 eclipse로 인식한다.

```css
.grad{
    background: red; /* css3 미지원 브라우저 */
    background: -webkit-radial-gradient(circle, white, yellow, red); /* 초기 사파리용 */
    background: -moz-radial-gradient(circle, white, yellow, red); /* 초기 파이어폭스용 */
    background: -o-radial-gradient(circle, white, yellow, red); /* 초기 오페라용 */
    background: radial-gradient(circle, white, yellow, red); /* 표준 구문 */
}
```

#### 위치

**표준 구문**에서는 '모양'과 '크기'속성 다음에 **at키워드와 함께** 위치 값을 지정하는데 **브라우저 접두사**를 붙이는 구문에서는 **at키워드 없이** 구문의 맨 앞부분에 위치를 표시한다. 생략하면 가로와 세로 모두 중앙인 center로 인식한다.

```css
.grad{
    background: blue; /* css3 미지원 브라우저 */
    background: -webkit-radial-gradient(10% 10%, circle, white, blue); /* 초기 사파리용 */
    background: -moz-radial-gradient(10% 10%, circle, white, blue); /* 초기 파이어폭스용 */
    background: -o-radial-gradient(10% 10%, circle, white, blue); /* 초기 오페라용 */
    background: radial-gradient(circle at 10% 10%, circle, white, blue); /* 표준 구문 */
}
```

#### 크기

원의 모양을 나타내는 키워드 값\(circle or eclipse\)과 크기를 나타내는 키워드 값을 함께 쓰면 된다.

##### 크기를 나타내는 키워드 값

* closest-side\(가장 가까운 모서리\) : 가장 가까운 모서리에 그러데이션 가장자리가 닿을 때까지 그러데이션을 그린다.
* closest-corner\(가장 가까운 코너\) : 그러데이션 가장자리가 그러데이션 중심에서 가장 가까운 요소의 코너에 닿도록 한다.
* farthest-side\(가장 먼 모서리\) : 그러데이션 가장자리가 그러데이션 중심에서 가장 먼 모서리와 만나거나 타원의 경우, 그러데이션 가장자리가 그러데이션 중심에서 가장 먼 모서리와 만나도록 한다.
* farthest-corner\(가장 먼 코너\) : 그러데이션 가장자리가 그러데이션 중심에서 가장 먼 코너에 닿도록 한다. 기본 값.

```css
.grad{
    background: darkgreen; /* css3 미지원 브라우저 */
    background: -webkit-radial-gradient(30% 40%, circle closest-side, white, yellow, green); /* 초기 사파리용 */
    background: -moz-radial-gradient(30% 40%, circle closest-side, white, yellow, green); /* 초기 파이어폭스용 */
    background: -o-radial-gradient(30% 40%, circle closest-side, white, yellow, green); /* 초기 오페라용 */
    background: radial-gradient(circle closest-side at 30% 40%, white, yellow, green); /* 표준 구문 */
}
```

#### 색상 중지 점\(color-stop\)

선형 그러데이션처럼 원형 그러데이션에서 색상이 바뀌는 부분을 색상 중지 점\(color-stop\)이라고 하는데 그러데이션 색상뿐만 아니라 색상이 바뀌는 위치도 함께 지정할 수 있다.

```css
.grad{
    background: skyblue; /* css3 미지원 브라우저 */
    background: -webkit-radial-gradient(red, yellow 20%, skyblue); /* 초기 사파리용 */
    background: -moz-radial-gradient(red, yellow 20%, skyblue); /* 초기 파이어폭스용 */
    background: -o-radial-gradient(red, yellow 20%, skyblue); /* 초기 오페라용 */
    background: radial-gradient(red, yellow 20%, skyblue); /* 표준 구문 */
}
```

### 그러데이션 반복

선형 그러데이션을 반복할 때는 **repeating-linear-gradient**,

원형 그러데이션의 반복은 **repeating-radial-gradient**를 사용한다.

```css
.grad1{
    background: red; /* css3 미지원 브라우저 */
    background: -webkit-repeating-linear-gradient(yellow, red 20px); /* 초기 사파리용 */
    background: -moz-repeating-linear-gradient(yellow, red 20px); /* 초기 파이어폭스용 */
    background: -o-repeating-linear-gradient(yellow, red 20px); /* 초기 오페라용 */
    background: repeating-linear-gradient(yellow, red 20px); /* 표준 구문 */
}

/* 시작 색상과 끝 색상을 명확히 구분해 주면 색상이 중간에 섞이지 않고 두 개 이상의 색상을 반복적으로 표시할 수 있다. */
.grad2{
    background: red; /* css3 미지원 브라우저 */
    background: -webkit-repeating-linear-gradient(yellow, yello 20px, red 20px, red 40px); /* 초기 사파리용 */
    background: -moz-repeating-linear-gradient(yellow, yello 20px, red 20px, red 40px); /* 초기 파이어폭스용 */
    background: -o-repeating-linear-gradient(yellow, yello 20px, red 20px, red 40px); /* 초기 오페라용 */
    background: repeating-linear-gradient(yellow, yello 20px, red 20px, red 40px); /* 표준 구문 */
}

/* 원형 그러데이션의 경우 */
.grad3{
    background: repeating-radial-gradient(circle, white, #ccc 10%);
}
.grad4{
    background: repeating-radial-gradient(circle, white, white 10%, #ccc 10%, #ccc 20%);
}
```



