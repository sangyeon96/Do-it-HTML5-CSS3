# 04-5 기타 다양한 폼 요소들

### &lt;button&gt; 태그 - 버튼 넣기

```php
<!-- 폼을 서버로 전송 -->
<button type="submit">내용</button>

<!-- 폼에 입력한 모든 내용을 초기화 -->
<button type="reset">내용</button>

<!-- 버튼 형태만 만들 뿐 자체 기능은 없다 -->
<button type="button">내용</button>
```

### &lt;output&gt; 태그 - 계산 결과

```php
<form oninput="result.value=parseInt(num1.value)+parseInt(num2.value)">
    <input type="number" name="num1" value="0">
    +<input type="number" name="num2" value="0">
    =<output name="result" for="num"></output> <!-- 결과 값 출력 -->
</form>
```

### &lt;progress&gt; 태그 - 진행 상태 보여주기

#### &lt;progress&gt; 태그의 속성

* **value** : 작업 진행 상태를 나타내며 부동 소수점으로 표현한다.
* **max** : 작업이 완료되려면 얼마나 많은 작업을 해야 하는지 부동 소수점으로 표현한다.

```php
<ul>
    <li>
        <label>10초 남음</label>
        <!-- 전체 60초 중 50초 진행 -->
        <progress value="50" max="60"></progress>
    </li>
    <li>
        <label>진행률 30%</label>
        <!-- 전체 100 중 30만큼 진행 -->
        <progress value="30" max="100"></progress>
    </li>
</ul>
```

### &lt;meter&gt; 태그 - 값이 차지하는 크기 표시하기

&lt;progress&gt; 태그와 &lt;meter&gt; 태그는 다르다.

&lt;progress&gt; 태그와 달리 &lt;meter&gt; 태그는 전체 크기 중에서 얼마나 차지하는지를 표현할 때 사용한다.

&lt;meter&gt; 태그는 작업이 진행된다는 의미보다 하드 디스크 전체 용량 중 사용량이나 투표율처럼 지정된 범위 내에서 해당 값이 어느 정도 차지하고 있는지를 표현한다.

#### &lt;meter&gt; 태그의 속성

* **min**, **max** : 범위의 최솟값과 최댓값을 나타낸다.
* **value** : 범위 내에서 차지하는 값을 나타낸다.
* **low** : "이 정도면 낮다."라고 할 정도의 값을 지정한다.
* **high** : "이 정도면 높다."라고 할 정도의 값을 지정한다.
* **optimum** : "이 정도면 적당하다."라고 할 정도의 범위를 지정한다.

```php
<ul>
    <li>
        <label>점유율 0.8</label>
        <!-- 전체 크기 1을 기준으로 0.8만큼 차지한다 -->
        <meter value="0.8"></meter>
    </li>
    <li>
        <label>사용량 64%</label>
        <!-- 전체 100 중에서 64만큼 차지한다 -->
        <meter min="0" max="100" value="64"></meter>
    </li>
    <li>
        <label>트래픽 초과</label>
        <!-- 전체 크기는 1024~10240인데 높다고 설정한 8192보다 현재 값 9216이 더 크다 -->
        <meter min="1024" max="10240" high="8192" value="9216"></meter>
    </li>
    <li>
        <label>적절한 트래픽</label>
        <!-- 전체 1 중에서 현재 0.5를 차지하고 있으며 적정도를 0.8로 설정했다 -->
        <meter value="0.5" optimum="0.8"></meter>
    </li>
</ul>
```



