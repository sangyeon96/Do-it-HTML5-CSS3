# 06-1 글꼴 관련 스타일

### font-family 속성 - 글꼴 지정하기

```css
body {
    font-family:"맑은 고딕", 돋움, 굴림
}
```

이렇게 하면, 웹 문서 전체에 "맑은 고딕"이라는 글꼴을 적용할 때 만약 "맑은 고딕" 글꼴이 없다면 "돋움" 글꼴로 적용하고 그 글꼴마저 없다면 "굴림" 글꼴로 적용하라는 의미이다.

### @font-face 속성 - 웹 폰트 사용하기

**웹 폰트\(web font\)**란 웹 문서를 작성할 때 웹 문서 안에 글꼴 정보도 함께 저장했다가 사용자가 웹 문서에 접속하면 글꼴을 사용자 시스템으로 다운로드시키는 방식이다. 결국 사용자 시스템에 없는 글꼴이더라도 웹 문서를 통해 필요한 글꼴들을 사용자 컴퓨터에 다운로드한 후 표시하기 때문에 웹 제작자가 의도한 대로 텍스트를 표시할 수 있다.

```php
<!DOCTYPE html>
<html lang="ko">
<head>
    <meta charset="utf-8">
    <title>웹 폰트 사용하기</title>
    <style>
      @import url(http://fonts.googleapis.com/earlyaccess/nanumgothic.css);  /* 구글 웹 폰트 */
      .ng-font {
        font-family:'Nanum Gothic', 돋움;  /* 웹 폰트 지정 */
      }
      p {
        font-size:30px; /* 글자 크기 */
      }
    </style>
</head>
<body>
  <p>브라우저 기본 글꼴 사용</p>
  <p class="ng-font">나눔고딕 웹 폰트 사용</p>
</body>
</html>
```

### font-size 속성 - 글자 크기 조절하기

주로 **px단위**\(픽셀. 모니터에 따라 상대적 크기가 된다.\)를 많이 사용하는데, 그 외 em, ex, pt단위도 있다.

px단위를 사용하면 폰트 크기가 고정되기 때문에 창 크기가 작은 모바일 기기로 볼 때도 같은 크기로 화면에 표시된다. 결국 작은 화면 안에 작은 글씨로 표시된다. 따라서 **모바일 기기**에서 접속할 경우까지 고려한다면 px단위보다 **em단위**\(해당 글꼴의 대문자 M의 너비를 기준으로 크기를 조절한다.\)를 사용하는 것이 좋다.

### font-weight 속성 - 글자 굵기 지정하기

* **normal** : 일반적인 형태

* **bold**/**lighter**/**bolder** : 굵게/원래 굵기보다 더 가늘게/원래 굵기보다 더 굵게

* **100~900** 사이의 수치 : 400\(normal\), 700\(bold\)

### font-variant 속성 - 작은 대문자로 표시하기

* **normal** : 일반적인 형태
* **small-caps** : 작은 대문자

### font-style 속성 - 글자 스타일 지정하기

* **normal** : 일반적인 형태
* **italic** : 이탤릭체
* **oblique** : 이탤릭체

### font 속성 - 글꼴 속성을 한꺼번에 묶어 표현하기

font 속성을 이용하면 font-style과 font-variant, font-weight, font-size/line-height\(줄 간격\), font-family 속성들을 한꺼번에 묶어 약식으로 표현할 수 있다.

_특정 키워드_를 입력해 그것에 어울리는 글꼴 스타일로 표시할 수 있는데, 밑에 참고.

```php
<!DOCTYPE html>
<html lang="ko">
<head>
    <meta charset="utf-8">
    <title>글꼴 스타일</title>
    <style>
        p.txt {
            font: italic 12px/24px 돋움;  /* font-style font-size/line-height font-family */
        }
    </style>
</head>
<body>
    <p class="txt">여러 요소가 함께 사용된 웹 문서 안에서 텍스트가 눈에 띄게 하려면 내용에 맞는 글꼴과 글자 크기, 그리고 글자색을 선택하는 것이 중요합니다. </p>
    <p>이럴 때 사용할 수 있는 것이 글꼴 속성입니다. </p>
    <p style="font:caption"> [font:caption] 캡션에 어울리는 글꼴 스타일</p>
    <p style="font:icon"> [font:icon] 아이콘에 어울리는 글꼴 스타일</p>
    <p style="font:menu"> [font:menu] 드롭다운 메뉴에 어울리는 글꼴 스타일</p>
    <p style="font:message-box"> [font:message-box] 대화 상자에 어울리는 글꼴 스타일</p>
    <p style="font:small-caption"> [font:small-caption] 작은 캡션에 어울리는 글꼴 스타일</p>
    <p style="font:status-bar"> [font:status-bar] 상태표시줄에 어울리는 글꼴 스타일</p>
</body>
</html>
```



