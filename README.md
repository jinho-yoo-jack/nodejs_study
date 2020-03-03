# # node.js
Test Bed Node.js Express And Javascript(ECMAScript6)

# Javascript
## 1. Data Type<br>
### 정의 : 
- javascript는 느슨한 타입(Loosely Typed) 언어, 또는 동적(Dynamic)언어 이다. 그 말은, `변수 선언 시 변수의 타입을 미리 선언할 필요가 없다`는 뜻이다. Type은 프로그램이 컴파일되는 과정에서 자동적으로 할당된다.
### 1.1 기본 자료형(Type Primitive)
1. Boolean<br>
`True` OR >`False`
```javascript
typeof true
// 'boolean'
```
2. Null<br>
No value, 값이 없다.
```javascript
typeof null
```
3. Undefined<br>
a declared variable but hasn't been given a value<br>
정의되어 있는 변수, 그러나 주어진 값은 없다. javascript에서는 변수를 선언하고 초기화 하지 않으면 `undefined` 초기화 된다.
```javascript
typeof undefined // 'undefined'
```
4. Number<br>
배정밀도 64비트 형식 IEEE 754 값 (-(2^53 -1)와 2^53-1 사이의 숫자 값<br>
정수만을 표현하기 위한 특별한 자료형은 없다.<br>
javascript에서만 존재하는 상징적인 값들이 존재(+/-Infinity, NaN)<br>
integer, floats, etc
```javascript
typeof Infinity // number
typeof 1.5      // number
```
5. String<br>
an array of characters i.e words<br
`String` 타입은 텍스트 데이터를 표현하는데 사용<br>
부호없는 16bit 정부 값 요소들의 집합<br>
자바스크립트의 문자열은 변경 불가능(Immutable)<br>
`탈출 문자(Escape character)`등을 사용하게 되면 복잡한 자료구조도 문자열로 표현할 수 있다.
```javascript
typeof 'a' // String
```
6. Symbol<br>
a unique value that's not equal to any other value<br>
유니크한 값, 그 어떠한 동일한 값도 없다.<br>
ECMAScript6에서 새롭게 추가된 데이터 타입, 유일하고 변경 불가능한(immutable) 기본 값
```javascript
typeof Symbol('a') // Symbol
Symbol('a') === Symbol('a') // false
```
7. *Function*
- 큰 프로그램을 잘게 쪼개어 특정 코드 뭉치를 반복해서 사용할 수 있도록 묶어놓은 코드 뭉치의 단위<br>
- 함수를 어떻게 작성하느냐에 따라서 코드의 유지보수성과 가독이 크게 달라지고, javascript에서는 함수가 가지고 있는 힘이 강하기 때문에 함수의 중요성이 높다.
```javascript
// 7-1. Default Function
function add(x,y){
    const result = x+y;
    return result;
}

// 7-2. Call Function
add(1,2); // return 3

```
7-1. function 이라는 키워드를 이용하여 함수정의를 시작하고 `add`라는 함수이름을 가지고, `x`와`y`는 `매개변수(parameter)`라 하며 `return`키워드는 반환값(return value)라고 한다.<br>
7-2. 함수를 선언한 이후에는 적절한 시점에 반드시 function을 호출해야 함수가 실행된다. 호출하는 방법은 이렇게 `함수이름(arg1,arg2, ....);` 호출하면 된다. 괄호 안에 넘겨준 1,2을 인수(argument)라고 부른다.<br>

7-3. parameter and argument<br>


### 1.2 Object
@속성
- 객체는 여러가지 데이터 타입(Type)을 담을 수 있는 Container이며 <br>
- 데이터의 형태는 키와 값(Key-Value) 한 쌍(Pair)의 형식 데이터를 저장한다.<br>
- 이렇게 저장된 데이터를 `속성(Property)` 이라 부른다.<br>
- 속성의 Key 를 식별자(Identifier)라고 하며, 식별자에 사용하지 못하는 문자열을 사용하는 경우에는 `반드시 문자열 표기`를 사용해야 한다.<br>
- 속성의 Value로는 어떠한 값(Literal Value, Array, etc ...)이든 저장할 수 있으며, 함수를 저장하고 있는 property를 Method(메소드)라고 한다.<br>
```javascript
// Object Literal
const obj = {
    company : 'i-bricks',
    name : 'YJH',
    sayHello : () => {
        return 'Hello Javascript';
    },
    skills : ['node.js','javascript/ajax/jquery','Elasticsearch','DB_SQL'],
    '한국 나이' : 20
};
```
- 속성 설정
```javascript
// @Object Property Accessor
const obj1 = {}; // Empty Object

// 1. Write Property
obj1.company = 'TEST'; // Dot notation : 객체 속성 접근법 중 가장 흔한 방법
obj1['한국 나이'] = 20;  // Bracket notation : 객체 속성의 식별자에 허용되지 않는 문자를 사용하는 경우 사용

// 2. Read Property
console.info(obj1.company);     // 'TEST' 출력
console.info(obj1['한국 나이']);  // 20 출력

// 3. Add New Property
obj1.name = 'LYJ';
obj1['한국 회사명'] = '아이브릭스';

// 4. Delete Property
delete obj1.name;

// 5. Check for Object Property Existence
'name' in obj1;     // false
'company' in obj1;  // true

// 6. Modify Property Value
obj1.name = 'LYJ';
console.log(obj1.name); // LYJ
obj1.name = 'Lim';
console.log(obj1.name); // Lim

```
@메소드(Method)
- 객체의 속성 값으로 Type Function를 가지는 속성을 메소드라고 부른다.<br>
- 메소드 안에서는 'this'라는 키워드를 사용할 수 있으며, 'this'는 메소드 호출 시에 해당하는 메소드를 갖고 있는 객체를 가리킨다.<br>
- 메소드를 사용하면 데이터와 그 데이터와 관련된 동작을 객체라는 하나의 단위로 묶어서 다룰 수 있게 된다. 이 부분이 함수 대신 메소드를 사용하는 이유이다.<br>
```javascript
// @Object Method
let obj2 = {
    name : 'JHY',
    sayBye : function(){
        // 여기서 'this'는 obj2를 가리키며 name 속성 값에 접근 할 수 있다.
        return `GoodBye ${this.name}`;
    }
};
console.log(obj2.sayBye()); // 출력 : GoodBye JHY
```



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
