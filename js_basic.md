# JavaScript 기본
## 특징
* 객체 기반(Object-based)의 스크립트 언어(Scripting Language)
* 또는 프로토타입 기반 언어(Prototype-based)
  * 프로토타입 기반 프로그래밍은 OOP스타일 중 하나이다.
* 인터프리터 언어
  * 웹의 동작을 구현(동적)
  * 타입을 명시할 필요 없음
* 객체 지향 프로그래밍과 함수형 프로그래밍(일급함수) 지원
> * 프레임워크를 사용하여 서버 프로그래밍도 가능(ex-Node.js)
> * 자바와 무관하다.
> * HTML의 내용, 속성, 스타일 변경가능

<br>

## 표준
* ECMAScript가 표준(ES6이 최신 표준; ECMAScript 2015)
	* 지원 브라우저 : http://kangax.github.io/compat-table/es6/
* 첫 버젼 : ECMA-262
* https://developer.mozilla.org/ko/docs/Web/JavaScript 참고

<br>

## 문법
* 세미콜론(;)으로 실행문 구분
* 대소문자 구분
	* 변수, 함수 이름, 예약어 작성 및 사용시 정확히 구분

<br>

### 리터럴(literal)
직접 표현되는 값 그 자체
```js
12				//숫자 리터럴
"JavaScript" 	// 문자열 리터럴
true		 	// 불리언 리터럴
```

<br>

### 식별자(identifier)

* 변수나 함수의 이름을 작성할 때 사용하는 이름
* 영문자(대소문자), 숫자, \_(underscore), $(달러) 사용 가능
* 숫자로 시작하면 안된다.
* 유니코드 문자셋(UCS; Unicode Charactor Set) 사용
* 카멜 표기법(Camel Case) 혹은 스네이크 표기법(Snake Case;UnderScore Case)을 따른다.
  * 관행적으로 카멜 표기법을 많이 사용한다.

<br>

### 키워드(keyword)

* 자바스크립트에서 특별한 용도로 사용하기 위해 만든 예약어(reserved word)
* 키워드는 프로그램 내에서 식별자로 사용할 수 없다.

<br>

### 주석(comment)

```js
// 한 줄 주석
/*
 * 여러 줄 주석
 * // 주석 안의 주석
 */
```

---

<br>

## 출력
여러 방법을 통해 출력 가능하다.

1. window.alert() 메소드
2. innerHTMP 프로퍼티(HTML DOM요소 이용)
3. document.write() 메소드
4. console.log() 메소드

### window.alert() 
* 가장 간단하게 데이터 출력 할 수 있는 방법
* 브라우저와 별도의 대화 상자를 띄워 데이터 전달.

![alert](assets/alert.PNG)

<br>

### innerHTML 프로퍼티

가장 많이 사용되는 방법

1. HTML 요소 선택
	* `document`객체의 `getElementByID()` 혹은 `getElementsByTagName()` 등의 메소드 사용 
2. `innerHTML`프로퍼티를 이용하여 선택된 HTML요소의 내용(content)이나 속성(attribute) 값 변경

<br>

### document.write()
* 웹 페이지가 로딩 될 때 실행되면, 가장 먼저 데이터 출력
	* 웹 페이지 내용이 로딩 된 후에 실행되면, 먼저 로딩된 데이터를 지우고 데이터 출력
* 테스트나 디버깅을 위해 사용

<br>

### console.log()
* 웹 브라우저 콘솔을 통해 데이터 출력
* 보다 자세한 사항까지 출력
* 디버깅에 사용

<br>

## 자바스크립트 적용
HTML문서에 자바스크립트 코드를 적용하는 방법으로
1. 내부 자바스크립트 코드로 적용하는 방법과
2. 외부 자바스크립트 파일로 적용하는 방법이 있다.

<br>

### 내부 자바스크립트 코드
* `<script>` 태그를 사용하여 문서 안에 삽입 가능
* `<head>` 태그 안이나 `<body>` 태그 안에서, 또는 둘 다 삽입 가능
  * 동작 상 차이는 없다.

<br>

### 외부 자바스크립트 파일
* 외부 파일로 생성하여 삽입 가능
* `.js` 확장자를 사용하여 저장
* 해당 자바스크립트 파일을 적용하고 싶은 페이지에 `<script>` 태그를 사용하여 삽입 가능
* 웹 브라우저가 미리 읽어 올 수 있어 로딩 속도가 빨라진다.


