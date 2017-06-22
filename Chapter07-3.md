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
    background: -webkit-linear-gradient(45deg, #0000ff, #ffffff); /* 초기 사파리용(끝부분 각도, 시작 색상, 끝 색상) */
    background: -moz-linear-gradient(45deg, #0000ff, #ffffff); /* 초기 파이어폭스용(끝부분 각도, 시작 색상, 끝 색상) */
    background: -o-linear-gradient(45deg, #0000ff, #ffffff); /* 초기 오페라용(끝부분 각도, 시작 색상, 끝 색상) */
    background: linear-gradient(45deg, #0000ff, #ffffff); /* 표준 구문(끝부분 각도, 시작 색상, 끝 색상) */
}
```

#### 색상 중지 점\(color-stop\)

선형 그러데이션을 만들기 위해서는 바뀌는 부분의 색을 지정해 주어야 하는데 바뀌는 지점을 **색상 중지 점\(color-stop\)**이라고 한다.

```css
.grad{
    background: #0000ff; /* css3 미지원 브라우저 */
    background: -webkit-linear-gradient(45deg, #0000ff, #ffffff); /* 초기 사파리용(끝부분 각도, 시작 색상, 끝 색상) */
    background: -moz-linear-gradient(45deg, #0000ff, #ffffff); /* 초기 파이어폭스용(끝부분 각도, 시작 색상, 끝 색상) */
    background: -o-linear-gradient(45deg, #0000ff, #ffffff); /* 초기 오페라용(끝부분 각도, 시작 색상, 끝 색상) */
    background: linear-gradient(45deg, #0000ff, #ffffff); /* 표준 구문(끝부분 각도, 시작 색상, 끝 색상) */
}
```

### 원형 그러데이션

### 그러데이션 반복



