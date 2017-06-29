# 13-2 변형과 관련된 속성들

### **transform-origin **속성 - 변형 기준점 설정하기

```css
transform-origin: <x축> <y축> <z축> | initial | inherit;
```

#### 속성 값

* &lt;x축&gt; : 길이 값, 백분율, left, center, right

* &lt;y축&gt; : 길이 값, 백분율, top, center, bottom

* &lt;z축&gt; : 길이 값

### **perspective**, **perspective-origin **속성 - 원근감 표현하기

3차원 변형에서 사용하는 속성, 원래 위치에서 사용자가 있는 방향이나 반대방향으로 잡아당기거나 밀어내 원근감을 갖게한다.

```css
/* 기본형 */
perspective: <크기> | none;
perspective-origin: <x축 값> | <y축 값>;
```

#### perspective 속성 값

* 크기
* none : 기본 값.

#### perspective-origin 속성 값

* &lt;x축 값&gt; : 길이 값, 백분율, left, center, right. 기본 값은 50%이다.
* &lt;y축 값&gt; : 길이 값, 백분율, top, center, bottom. 기본 값은 50%이다.

### **transform-style** 속성 - 3D 변형 적용하기

부모 요소에 적용한 3D변형을 하위 요소에도 적용할 수 있다.

```css
transform-style: flat | preserve-3d
```

#### 속성 값

* **flat** : 하위 요소를 평면으로 처리한다.
* **preserve-3d** : 하위 요소들에 3D효과를 적용한다.

### **backface-visibility** 속성 - 요소의 뒷면 표시하기

요소의 뒷면, 즉 반대쪽 면을 표시할 것인지를 결정한다.

```css
backface-visibility: visible | hidden
```

#### 속성 값

* visible : 기본 값.
* hidden



