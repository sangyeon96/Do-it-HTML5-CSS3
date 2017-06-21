# 07-1 웹에서 색상 표현하기

### 16진수 표기법

ex\) **\#ffff00 **\(yellow\)

이 6자리는 앞에서부터 두 자리씩 묶어 \#RRGGBB 형식으로 표시한다.

**RR\(Red\), GG\(Green\), BB\(Blue\)**을 각 색상마다 하나도 섞이지 않았음을 표시하는 00부터 해당 색이 가득 섞였음을 표시하는 ff까지 사용할 수 있는 값은 \#000000\(검은색\)~\#ffffff\(흰색\)까지이다.

### rgb와 rgba 표기법

**rgb**\(red값, green값, blue값\)

**rgba**\(red값, green값, blue값, alpha값\)

alpha값은 불투명도 값을 나타낸다.

### hsl과 hsla 표기법

**hsl**\(hue값, saturation값, lightness값\)

**hsla**\(hue값, saturation값, lightness값, alpha값\)

![](/assets/hsl-color-wheel.png)

출처 : [https://tympanus.net/codrops/css\_reference/hsl/](https://tympanus.net/codrops/css_reference/hsl/)

**hue**\(색상\)은 색의 3요소 중 하나로 각도를 기준으로 색상을 둥글게 배치한 색상환으로 표시한다.

0도와 360도에는 빨간색, 120도에는 초록색, 240도에는 파란색이 배치되고 그 사이사이에 나머지 색들이 배치된다.

**saturation**\(채도\)는 색의 3요소 중 하나로 '%'로 표시하는데 아무 것도 섞이지 않은 상태가 채도가 가장 높은 상태이다.

채도가 0%면 회색 톤, 100%면 순색으로 표시된다.

**lightness**\(밝기\)도 %로 표시하는데 0%가 가장 어둡고 100%가 가장 밝다.

### 색상 이름 표기법

```css
.color_notation{
    color:#ff0000; /* 빨간색 */
    color:rgb(255, 255, 255); /* 흰색 */
    color:rgba(255, 255, 255, 0.8); /* 투명도 0.8인 흰색 */
    color:hsl(0, 100%, 50%); /* 채도 100% 밝기 50%인 빨간색 */
    color:hsla(0,100%,50%,0.6); /* 채도 100% 밝기 50% 불투명도 0.6인 빨간색 */
}
```

### 색상 추출 사이트 이용하기

Color Picker\([http://www.colorpicker.com\)](http://www.colorpicker.com)

