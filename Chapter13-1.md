# 13-1 변형

### 2차원 변형과 3차원 변형

**2차원 변형\(2D transform\)**은 웹 요소를 변형시킬 때 단순히 수평이나 수직으로 이동하고 회전하는 것,

**3차원 변형\(3D transform\)**은 x축과 y축에 원근감을 주는 z축을 추가해 변형시키는 것을 말한다.

### transform과 변형 함수

```css
/* 기본형 */
transform: 변형함수;

/* 예시 */
.photh{ transform: translate(50px, 100px); }
```

최신 브라우저에서는 모두 지원되지만 인터넷 익스플로러 9를 비롯한 이전 브라우저는 브라우저 접두사\(-webkit-, -moz-, -ms-, -o-\)를 붙여야한다.

#### 2차원 변형 함수

* **translate\(tx, ty\)** : 지정한 크기만큼 x축과 y축으로 이동
* **translateX\(tx\)** : 지정한 크기만큼 x축으로 이동
* **translateY\(ty\)** : 지정한 크기만큼 y축으로 이동
* **scale\(sx,sy\)** : 지정한 크기만큼 x축과 y축으로 확대/축소
* **scaleX\(sx\)** : 지정한 크기만큼 x축으로 확대/축소
* **scaleY\(sy\) **: 지정한 크기만큼 y축으로 확대/축소
* **rotate\(각도\)** : 지정한 각도만큼 회전
* **skew\(ax,ay\)** : 지정한 각도만큼 x축과 y축으로 왜곡
* **skewX\(ax\)** : 지정한 각도만큼 x축으로 왜곡
* **skewY\(ay\) **: 지정한 각도만큼 y축으로 왜곡

#### 3차원 변형 함수

* **matrix3d\(n,\[,n\]\)** : 4\*4행렬을 이용해 이동과 확대/축소,회전 등의 변환 지정
* **translate\(tx, ty, tz\)** : 지정한 크기만큼 x축과 y축, z축으로 이동
* **translateZ\(tz\)** : 지정한 크기만큼 z축으로 이동
* **scale3d\(sx, sy, sz\)** : 지정한 크기만큼 x축과 y축, z축으로 확대/축소한다.
* **scaleZ\(sz\)** : 지정한 크기만큼 z축으로 확대/축소
* **rotate3d\(rx,ry,rz,각도\)** : 지정한 각도만큼 회전
* **rotateX\(각도\)** : 지정한 각도만큼 x축으로 회전
* **rotateY\(각도\)** : 지정한 각도만큼 y축으로 회전
* **rotateZ\(각도\)** : 지정한 각도만큼 z축으로 회전
* **perspective\(길이\)** : 입체적으로 보일 수 있는 깊이 값을 지정

### **translate** 변형 함수 - 요소 이동시키기

```css
/* 기본형 */
transform:translate(tx, ty)
transform:translate3d(tx, ty, tz)
transform:translateX(tx)
transform:translateY(ty)
transform:translateZ(tz)
```

### **scale **변형 함수 - 요소 확대/축소하기

```css
/* 기본형 */
transform:scale(sx, sy)
transform:scale3d(sx, sy, sz)
transform:scaleX(sx)
transform:scaleY(sy)
transform:scaleZ(sz)
```

### **rotate** 변형 함수 - 요소 회전하기

```css
/* 2차원 함수 기본형 */
transform:rotate(각도)

/* 3차원 함수 기본형 */
transform:rotate(rx, ry, 각도)
transform:rotate3d(rx, ry, rz, 각도)
transform:rotateX(각도)
transform:rotateY(각도)
transform:rotateZ(각도)
```

### **skew** 변형 함수 - 요소를 비틀어 왜곡하기

```css
/* 기본형 */
transform:skew(ax, ay)
transform:skewX(ax)
transform:skewY(ax)
```



