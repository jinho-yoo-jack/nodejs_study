# # node.js
Test Bed Node.js Express And Javascript(ECMAScript6)

# Javascript
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
