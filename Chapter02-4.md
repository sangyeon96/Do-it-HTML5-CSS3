# 02-4 표를 만드는 태그

표\(table\)

**행\(row\)** - 가로, **열\(column\)** - 세로

**셀\(cell\) **- 행과 열이 만나 이루는 영역

### &lt;table&gt;, &lt;tr&gt;, &lt;td&gt;, &lt;th&gt; 태그 - 기본적인 표 만들기

th table heading

#### 기본적인 표 만들기

1. &lt;table&gt; 태그를 이용해 표 전체 윤곽을 잡는다.
2. &lt;tr&gt; 태그를 이용해 행\(row\)을 먼저 만든다.
3. &lt;td&gt; 태그를 이용해 각 행마다 몇 개의 셀\(cell\)이 들어갈지 결정한다.

```php
<table>
    <!-- table row -->
    <tr>
        <!-- table data -->
        <td>내용</td>
        <td>내용</td>
        <td>내용</td>
    </tr>
    <tr>
        <td>내용</td>
        <td>내용</td>
        <td>내용</td>
    </tr>
</table>
```

#### &lt;th&gt; 태그 - 표에 제목 셀 만들기

```php
<table border="1"> <!-- 표에 테두리 표시 -->
    <tr>
        <!-- table heading -->
        <th>제목 셀(1행 1열)</th>
        <!-- table data -->
        <td>1행 2열</td>
        <td>1행 3열</td>
    </tr>
    <tr>
        <th>제목 셀(2행 1열)</th>
        <td>2행 2열</td>
        <td>2행 3열</td>
    </tr>
</table>
```

#### colspan, rowspan 속성 - 행 또는 열 합치기

여기서 헷갈릴 만한게 보기에는 가로를 합치는데 colspan을 쓰고, 세로를 합치는데 rowspan을 쓴다.

예를 들어 2행 3열 표라고 했을 때,

1행 _2열_과 1행 _3열_을 합칠 때 - 열을 합치므로 colspan

_1행_ 1열과 _2행_ 1열을 합칠 때 - 행을 합치므로 rowspan

이렇게 이해하면 될 듯 하다.

```php
<!-- 열 합치기(가로) -->
<th colspan="합칠 셀의 개수">내용</th>
<td colspan="합칠 셀의 개수">내용</td>

<!-- 행 합치기(세로) -->
<th rowspan="합칠 셀의 개수">내용</th>
<td rowspan="합칠 셀의 개수">내용</td>
```

### &lt;caption&gt; 태그, &lt;figcaption&gt; 태그 - 표에 제목 붙이기

|  | &lt;caption&gt; 태그 | &lt;figcaption&gt; 태그 |
| :--- | :--- | :--- |
| 의미 | caption | figure + caption |
| 위치 | 위쪽 중앙 | 표 위 아래 둘 다 가능 |

#### &lt;caption&gt; 태그 사용하기

&lt;caption&gt; 안에는 다른 태그를 사용해 제목을 여러 줄로 표시하거나 텍스트를 꾸밀 수도 있다.

```php
<table border="1">
    <caption>
        <strong>표 제목</strong>
        <p>표 제목 설명</p>
    </caption>
    <tr>
        <th></th>
        <td></td>
    </tr>
</table>
```

#### &lt;figcaption&gt; 태그 사용하기

figure와 caption의 합성어.

설명 글을 붙이고 싶은 대상을 &lt;figure&gt; 태그로 감싼 후 &lt;figcaption&gt; 태그를 이용해 제목이나 설명 글을 입력한다.

&lt;caption&gt; 태그와 달리 중앙에 정렬되지 않는다. 또한 &lt;caption&gt; 태그를 사용하면 제목이 위쪽 중앙에 표시되는 반면, &lt;figcaption&gt; 태그를 &lt;table&gt; 태그보다 앞에 사용하면 표 위에 제목이 표시되고 &lt;/table&gt; 태그 다음에 추가하면 표 아래에 제목이 표시된다.

```php
<figure>
    <table border="1">
        <tr>
            <th></th>
            <td></td>
        </tr>
    </table>
    <figcaption>
        <p>[표1-1]표 설명<b>표 제목</b></p>
    </figcaption>
</figure>
```

#### aria-describedby 속성 - 표에 대한 설명 제공하기

화면 낭독기에서 표를 읽어줄 때 도움이 되도록 표 설명을 별도의 문장으로 작성한 후 &lt;table&gt; 태그 안에 aria-describedby 속성을 추가해 연결하면 표를 이해하는 데 도움이 된다.

```php
<p id="summary">표 설명</p>
    <table border="1" aria-describedby="summary">
        <caption>표 제목</caption>
        <tr></tr>
    </table>
```

### &lt;thead&gt;, &lt;tbody&gt;, &lt;tfoot&gt; 태그 - 표 구조 정의하기

### &lt;col&gt;, &lt;colgroup&gt; 태그 - 여러 열 묶어 스타일 지정하기



