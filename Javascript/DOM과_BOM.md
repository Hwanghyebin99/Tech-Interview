# 📑DOM과 BOM
## 목차
  1. [문서 객체 모델(DOM)](#DOM-(Document-Object-Model))
  2. [브라우저 객체 모델(BOM)](#BOM-(Browser-Object-Model))

## DOM (Document Object Model)
### 문서 객체 모델(DOM)
DOM은 XML, HTML 문서에 접근하기 위한 인터페이스이며 계층 구조로 표현된다.  
DOM은 웹 페이지를 객체로 표현해주며, 자바스크립트와 같은 스크립팅 언어로 웹 페이지에 접근할 수 있는 방법을 제공하여 구조, 스타일, 내용을 변경할 수 있도록 도와준다.

예를 들어 자바스크립트에서 HTML의 \<h1> element들에 접근을 하는 방법은 다음과 같다.
```Javasript
var headElement = document.getElementsByTagName('h1');
```
DOM tree 구조에서 자주 사용되는 노드는 다음과 같다
* Document: 트리의 최상단
* Element: TAG
* Attribute: element의 속성
* Text: 트리의 최종단
## BOM (Browser Object Model)
### 브라우저 객체 모델(BOM)
BOM은 웹 브라우저 전체를 객체로 표현하며 스크립팅 언어로 웹 브라우저를 조작할 수 있도록 해준다.
다음은 자바스크립트로 BOM 객체를 이용해 현재 브라우저의 URL 주소를 출력하는 코드이다.
```Javascript
console.log(location.href);
```
BOM에는 다음과 같은 객체가 있다.
<table>
    <tbody>
        <tr>
            <td>navigator</td>
            <td>브라우저 명과 버전 정보를 속성으로 가진다.</td>
        </tr>
        <tr>
            <td>window</td>
            <td>브라우저 요소들 중 최상위 객체이다.</td>
        </tr>
        <tr>
            <td>history</td>
            <td>현재 창에서의 사용자 방문 기록을 가진다.</td>
        </tr>
        <tr>
            <td>location</td>
            <td>현재 페이지에 대한 URL 정보를 다룬다.</td>
        </tr>
        <tr>
            <td>navigator</td>
            <td>현재 사용중인 웹 브라우저 정보를 다룬다.</td>
        </tr>
        <tr>
            <td>screen</td>
            <td>현재 사용중인 화면 정보를 다룬다.</td>
        </tr>
    </tbody>
</table>