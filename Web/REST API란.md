# 🔮RESTful API(Representational State Transfer)
  1. [개념](#개념) 
  2. [RESTful API](#RESTful-API)

## 개념
### REST API란
REST API란 REST 아키텍처의 제약조건을 준수하는 인터페이스를 뜻합니다.

### REST란?
REST는 Representational State Transfer의 약자로서 WWW와 같은 분산 하이퍼미디어 시스템을 위한 소프트웨어 아키텍처의 한 형식 입니다.

REST 형식은 자원을 정의하고 자원에 대한 주소를 지정하는 방법 전반을 일컫습니다.

## RESTful API
### 🔎REST의 특징
- 인터페이스 일관성
- 무상태  
각 요청 간 클라이언트의 콘텍스트가 서버에 저장되어서는 안 된다
- Cacheable  
클라이언트는 응답을 캐싱할 수 있어야 한다.
잘 관리되는 캐싱은 확장성과 성능을 향상시킨다.
- 계층화  
클라이언트는 보통 대상 서버에 직접 연결되었는지, 또는 중간 서버를 통해 연결되었는지를 알 수 없다.
- Code on demand (optional)  
서버가 클라이언트가 실행시킬 수 있는 로직을 전송하여 기능을 확장시킬 수 있다.
- 클라이언트/서버 구조
### 📜RESTful API의 설계 원칙
Restful api의 설계 원칙의 기본 두가지 원칙은 아래와 같습니다.
1. URI는 정보의 자원을 표현해야 한다.

2. 자원에 대한 행위는 HTTP Method(GET, POST, PUT, DELETE)로 표현한다.
#### 1.URI는 정보의 자원을 표현
```sh
#잘못된 표현
GET books/show/1
GET showBooks/1

#올바른 표현
get books/1
```
책 리스트의 id가 1인 book의 정보를 가져온다.
#### 2.자원에 대한 행위는 HTTP Method로 표현
<table>
    <thead>
        <tr>
            <th>METHOD</th>
            <th>역할</th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td>GET</td>
            <td>특정 리소스를 요청하며, GET은 오직 데이터를 받기만 합니다.</td>
        </tr>
        <tr>
            <td>POST</td>
            <td>리소스를 생성할 때 사용하며, 종종 서버의 상태의 변화나 부작용을 일으킵니다.</td>
        </tr>
        <tr>
            <td>DELETE</td>
            <td>리소스를 삭제할 때 사용한다.</td>
        </tr>
        <tr>
            <td>PUT</td>
            <td>리소스의 전체를 교체할 때 사용한다.</td>
        </tr>
        <tr>
            <td>PATCH</td>
            <td>리소스의 일부만 교체할 때 사용한다.</td>
        </tr>
    </tbody>
</table>