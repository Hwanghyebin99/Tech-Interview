# 🎨클로저(Closure)
## 목차
  1. [클로저가 무엇일까](#클로저가-무엇일까) 
  2. [클로저를 쓰는 이유](#클로저를-쓰는-이유)
## 클로저가 무엇일까
 클로저를 이해하려면 Lexial scoping에 대해서 먼저 이해해야 합니다.

### Lexical scoping이란
 함수의 호출이 아니라 함수의 선언에 따라 상위 스코프를 결정하는 것을 말합니다.  
 예를 들어
```Javascript
let number = 0;

function a() {
 let number = 10;
 b();
}

function b() {
  console.log(number);
}

a();
```
상위 스코프가 함수의 선언에 따라 결정되기 때문에 함수 b에서 사용한 number 변수는 호출한 함수 a의 number가 아닌 전역에 선언된 number가 들어갑니다.  
결과적으로 위 코드의 실행결과는
```
0
```
입니다. 
### 클로저란
클로저는 이런 렉시컬 스코핑과 함수의 조합으로 자신이 생성될 때의 lexical environment를 기억하는 함수이다.
예를 들어
```Javascript
let number = 0;

function a() {
  let number = 10;
  function b() {
    console.log(number);
  }
  //함수 반환
  return b;
}

let func = a();
//리턴된 b 함수를 실행
func();
```
함수 a를 실행하고 return 된 함수 b가 func 변수에 저장된다.   
리턴된 함수 b를 실행하게 되면 함수 a 실행은 끝났기 때문에 a의 지역변수인 number가 아닌 전역 변수 number를 출력할 것 같지만 콘솔에는 
```shell
 10
```
이 찍히는 것을 확인할 수 있다.  
10이 찍히는 이유는 b의 인스턴스가 a 함수의 lexical environment에 대한 참조를 유지하기 때문이다. 따라서 func를 호출하면 함수 a의 number에 접근가능해 진다. 이 때 func를 클로저라고 한다.

## 클로저를 쓰는 이유
클로저를 사용하면 객체 프로그래밍의 정보 은닉과 캡슐화를 따라할 수 있다. 또한 상태 유지를 이용하여 전역변수 사용을 억제할 수 있다.
