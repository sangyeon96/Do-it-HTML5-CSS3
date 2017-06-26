# 10-3 IE8 이하 버전에서는 어떻게 하나요?

### 새로운 시맨틱 태그 지원 상황

[http://caniuse.com](http://caniuse.com) - \[Index of features\] - 태그나 속성을 선택하면 그 항목을 모던 브라우저에서 얼마나 지원하는지 직접 확인할 수 있다.

### IE8 이하에서 시맨틱 태그를 사용하려면?

* CSS에서 블록 레벨로 정의하기
* 시맨틱 태그 직접 정의하기
* HTML5 Shiv 사용하기

책 참고.

### 브라우저 사이의 차이를 메꾸어 주는 폴리필\(pollyfill\)

브라우저 사이에 차이가 나는 것을 브라우저 파편화\(browser fragmentation\)라고 부른다.

이런 브라우저 파편화를 줄이고 비슷하게라도 같은 결과를 만들기 위한 방법을 통틀어 **심\(shim\)** 또는 **폴백\(fallback\)**이라고 부른다.

폴리필\(pollyfill\)은 파편화가 생기는 브라우저에 삽입하는 자바스크립트로 브라우저를 스스로 진단해 필요한 shim을 자동으로 끼워 넣어 준다.

HTML5 Cross Browser Pollyfills\([https://github.com/Modernizr/Modernizr/wiki/HTML5-Cross-Brower-Polyfills\)](https://github.com/Modernizr/Modernizr/wiki/HTML5-Cross-Brower-Polyfills)

