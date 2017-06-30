# 13-3 트랜지션

### 트랜지션이란

transition.

웹 요소의 배경 색이 바뀌거나 도형의 테두리가 원형으로 바뀌는 것처럼 스타일 속성이 바뀌는 것을 말한다.

### **transition-property** 속성 - 트랜지션을 적용할 속성 지정하기

#### 속성 값

* all : 기본 값.
* none
* &lt;속성 이름&gt;

```css
/* 예시 */
transition-property:all; /* 해당 요소의 모든 속성에 트랜지션 적용 */
transition-property:background-color; /* 해당 요소의 배경 색에 트랜지션 적용 */
transition-property:width, height; /* 해당 요소의 너비와 높이에 트랜지션 적용 */
```

### **transition-duration** 속성 - 트랜지션 진행 시간 지정하기

```css
/* 기본형 */
transition-duration: <시간>

/* 예시 */
transition-property:width, height;
transition-duration: 2s, 1s; /* 너비 값은 2초, 높이 값은 1초에 걸쳐 트랜지션 */
```

### **transition-timing-function** 속성 - 트랜지션 속도 곡선 지정하기

#### 속성 값

* **linear **: 시작부터 끝까지 똑같은 속도로 트랜지션을 진행한다.
* **ease **: 처음에는 천천히 시작하고 점점 빨라지다가 마지막에는 천천히 끝낸다. 기본 값.
* **ease-in **: 시작을 느리게 한다.
* **ease-out** : 느리게 끝낸다.
* **ease-in-out** : 느리게 시작하고 느리게 끝낸다.
* **cubic-bezier\(n,n,n,n\)** : 배지에 함수를 직접 정의해 사용한다. n에서 사용할 수 있는 값은 0~1이다.

### **transition-delay** 속성 - 지연 시간 설정하기

```css
#no-delay {
    transition-duration: 3s;
}
#delay {
    transition-duration: 3s;
    transition-delay: 1s; /* 1초 늦게 실행됨 */
}
```

### **transition **속성 - 트랜지션 속성 한꺼번에 표기하기

transition 속성 값의 나열 순서는 다음 순서를 따라야 한다. 4개의 속성 중 빠진 것이 있다면 그 속성의 기본 값을 사용한다.

```css
transition: <transition-property 값> | <transition-duration 값> | <transition-timing-function 값> | <transition-delay 값>
```



