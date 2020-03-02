# # node.js
Test Bed Node.js Express And Javascript(ECMAScript6)

# Javascript
## 1. Data Type<br>
### 정의 : 
- javascript는 느슨한 타입(Loosely Typed) 언어, 또는 동적(Dynamic)언어 이다. 그 말은, `변수 선언 시 변수의 타입을 미리 선언할 필요가 없다`는 뜻이다. Type은 프로그램이 컴파일되는 과정에서 자동적으로 할당된다.
### 1.1 기본 자료형(Type Primitive)
- Boolean<br>
`True` OR >`False`
```javascript
typeof true
// 'boolean'
```
- Null<br>
No value, 값이 없다.
```javascript
typeof null
```
- Undefined<br>
a declared variable but hasn't been given a value<br>
정의되어 있는 변수, 그러나 주어진 값은 없다. javascript에서는 변수를 선언하고 초기화 하지 않으면 >`undefined` 초기화 된다.
```javascript
typeof undefined // 'undefined'
```
- Number<br>
배정밀도 64비트 형식 IEEE 754 값 (-(2^53 -1)와 2^53-1 사이의 숫자 값<br>
정수만을 표현하기 위한 특별한 자료형은 없다.<br>
javascript에서만 존재하는 상징적인 값들이 존재(+/-Infinity, NaN)<br>
integer, floats, etc
```javascript
typeof Infinity // number
typeof 1.5      // number
```
- String<br>
an array of characters i.e words<br
`String` 타입은 텍스트 데이터를 표현하는데 사용<br>
부호없는 16bit 정부 값 요소들의 집합<br>
자바스크립트의 문자열은 변경 불가능(Immutable)<br>
`탈출 문자(Escape character)`등을 사용하게 되면 복잡한 자료구조도 문자열로 표현할 수 있다.
```javascript
typeof 'a' // String
```
- Symbol<br>
a unique value that's not equal to any other value<br>
유니크한 값, 그 어떠한 동일한 값도 없다.<br>
ECMAScript6에서 새롭게 추가된 데이터 타입, 유일하고 변경 불가능한(immutable) 기본 값
```javascript
typeof Symbol('a') // Symbol
Symbol('a') === Symbol('a') // false
```
### 1.2 Object
- 식별자(Identifier)로 참조할 수 있는 메모리에 있는 데이터<br>
- 자바스크립트에서 객체는 속성(Properties)들을 담고 있는 가방(Collection)<br>
- Object Literal Syntax)으로 제한적으로 몇가지 속성을 초기화 할 수 있고, 속성을 추가 또는 삭제가 가능<br>
- 속성 값은 객체를 포함해 어떠한 자료형도 될 수 있고, 이로 인해 복잡한 데이터 구조를 형성하는게 가능<br>
- 속성은 키(key) 값으로 식별되면 키 값의 데이터 타입은 String 또는 Symbol 값을 가진다.


## 1. What the hell Javascript?
## ES5/6의 수정 및 추가된 부분
### - Keyword 엄격 모드('use strict')
: 언어의 하위 집합으로 사용되지 않는 기능을 제외한다. 즉, 엄격 모드에서 코드를 실행하려면 다음 문자열을 사용하여 의도를 선언(함수당 한번, 또는 전체 프로그램에서 한번) 해야 한다. **strict 모드는 자바스크립트가 묵인했던 에러들의 에러 메시지를 발생시킵니다.**
ES6 부터는 자동으로 '엄격 모드'가 적용된다. Arrow 나 Generator 함수 같은 새로운 구조에서는 적용이 되지 않는다.
### -ES6 Template Literal
: template literal use back-tick and express place holder to "${express}"                                       
```c
let name = 'John', mood = 'happy';
console.log(`Hey ${name}, are you feeling ${mood} today?`);
```
```c
let a = 10;
let b = 10;
console.log(`Sum is ${a + b} and Multiplication would be ${a * b}.`);
```





## 2. JS 자료구조
### 2-1. LinkList<br>
#### a. 정의
#### b. 구현
#### c. 설명

## 3. ES6 문법 정리
### 1. Proxy
- 정의 : Proxy 객체는 기본적인 동작(속성 접근, 할당, 순회, 열거, 함수 호출 등)의 새로운 행동을 정의 할 때 사용.
- params : handler : trap들을 가지고 있는 Placeholder 객체
           traps : 프로퍼티에 접근 할 수 있는 메소드. 운영체제에서 trap 이라는 컨셉과 유사
           target : proxy가 가상화하는 실제 객체. 이것은 proxy를 위한 backend 저장소로 사용
