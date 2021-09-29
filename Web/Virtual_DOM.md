# 📑Virtual DOM
## 목차
  1. [Virtual DOM이란](#Virtual-DOM이란)
  2. [Virtual DOM 처리 방식](#Virtual-DOM-처리-방식)

## Virtual DOM이란
<a href="https://github.com/Hwanghyebin99/Tech-Interview/blob/master/Javascript/DOM%EA%B3%BC_BOM.md#DOM-(Document-Object-Model)">DOM</a>을 추상화한 가상의 객체이다.

Virtual DOM은 다음과 같은 문제를 해결하기 위해 도입되었다.
* DOM 조작에 의한 렌더링으로 인한 성능 저하
* SPA특징으로 DOM 복잡도 증가에 따른 최적화 및 유지보수가 어려워지는 문제

DOM tree의 노드에 변경이 일어날 때 마다 다음과 같은 과정을 거친다.
1. CSS의 재연산
2. 레이아웃
3. 리페인트

따라서 잦은 업데이트가 일어날 경우 성능 저하가 일어난다. 성능을 높이기 위해서는 DOM을 최소한으로 조작해야 한다.
DOM을 추상화한 Virtual DOM 방식을 사용하면 처리 횟수를 최소한으로 할 수 있다.  

## Virtual DOM 처리 방식
1. 변경이 일어나면 Virtual DOM 리렌더링
2. 실제 DOM과 리렌더링된 Virtual DOM을 비교
3. 변경된 부분만 실제 DOM에 적용
