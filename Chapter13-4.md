# 13-4 애니메이션

### CSS와 애니메이션

### **@keyframes** 속성 - 애니메이션 지점 설정하기

애니메이션 중간에 스타일이 바뀌는 지점을 **키프레임\(keyframe\)**이라고 한다.

```css
@keyframes <이름>{ <선택자> { <스타일> } }

@keyframes change-bg {
    from { /* 애니메이션 시작 시점 스타일 */
        background-color: blue;
        border: 1px solid black;
    }
    to { /* 애니메이션 끝 시점 스타일 */
        background-color: #a5d6ff;
        border:1px solid blue;
        border-radius: 50%;
    }
}
```

### **animation-name** 속성 - 애니메이션 이름 지정하기

```css
animation-name: <키프레임 이름> | none
```

### **animation-duration** 속성 - 애니메이션 실행 시간 설정하기

### **animation-direction** 속성 - 애니메이션 방향 지정하기

#### 속성 값

* normal : 애니메이션을 끝까지 실행하면 원래 있던 위치로 돌아간다. 기본 값.
* alternate : 애니메이션을 끝까지 실행하면 왔던 방향으로 되돌아가면서 애니메이션을 실행한다.

### **animation-iteration-count** 속성 - 반복 횟수 지정하기

#### 속성 값

* &lt;숫자&gt; : 입력한 숫자만큼 반복한다. 기본 값은 1이다.
* infinite : 무한 반복한다.

### **animation-timing-function** 속성 - 애니메이션 속도 곡선 지정하기

#### 속성 값

* **linear **: 시작부터 끝까지 똑같은 속도로 트랜지션을 진행한다.
* **ease **: 처음에는 천천히 시작하고 점점 빨라지다가 마지막에는 천천히 끝낸다. 기본 값.
* **ease-in **: 시작을 느리게 한다.
* **ease-out** : 느리게 끝낸다.
* **ease-in-out** : 느리게 시작하고 느리게 끝낸다.
* **cubic-bezier\(n,n,n,n\)** : 배지에 함수를 직접 정의해 사용한다. n에서 사용할 수 있는 값은 0~1이다.

### **animation** 속성 - 애니메이션 관련 속성 한꺼번에 표기하기

나머지 속성 값들은 표기하지 않을 시 기본 값을 사용하는데, animation-duration 속성 값은 반드시 표기해야 한다.

애니메이션 실행 시간을 지정하지 않으면 기본 값 0이 적용되어 애니메이션 효과를 볼 수 없기 때문이다.

다음의 기본형에 나열된 속성 값 순서대로 입력해야 한다.

```css
animation: <animation-name> | <animation-duration> | <animation-timing-function> | <animation-delay> | <animation-iteration-count> | <animation-direction>
```



