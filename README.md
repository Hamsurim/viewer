# 외부 API를 활용한 과학 뉴스 뷰어
들어가기 전에, 우선 API에 대해 알아보겠습니다.

API란?
API는 Application Programming Interface의 약자로, 다른 프로그램이나 서버와 데이터를 주고받을 수 있는 방법을 제공합니다. 클라이언트가 HTTP 요청을 보내면 서버는 그에 따른 응답을 제공하여 데이터를 교환할 수 있습니다.

매우 간단한 예시를 통해 설명하자면 피자를 하나 주문한다고 가정해보자 

1. 손님이 사장님에게 피자를 만들어 달라고 요구합니다.
2. 사장님은 손님의 요구사항을 확인하고 피자를 만들어 제공합니다.
3. 손님은 받은 피자를 먹거나 선물하거나 사진을 찍는 등 다양한 방식으로 활용할 수 있습니다.

여기서 손님은 클라이언트, 사장님은 서버이다. 
클라이언트가 HTTP GET 요청을 사용하여 서버에게 요청을 보내면, 서버는 해당 요청을 받고
데이터를 JSON 형식으로 응답해준다. 클라이언트는 받은 JSON데이터를 파싱(데이터를 추출)하여
화면에 표시하거나 다른 작업을 수행해주는 것이다. 

작동원리 까지 이해했다면 왜 api를 사용하는지 궁금해졌다. 

먼저 api가 주는 장점은 첫번째 통합성과 재사용성이 크게 향상된다. 기업이나 정부에서 제공하는 것을 
받아와 사용하면 되니까. 
두번째는 다양한 기술과 데이터를 유연하게 사용 할 수 있다. 카카오에서 지도앱 api를 제공한다 생각해보자
그 지도를 통해 어떤 사람은 내 위치를 알려주는 지도를, 다른이는 추천경로를 알려주는 지도 등 여러가지의 
애플리케이션이 나온다.

방법, 장점 다 알았고 그럼 이제 어떻게 사용하는데?
일단 api를 호출해서 데이터를 받아와야 한다. 그 중 axios 라는 자바스크립트 라이브러리가 있는데, 
주로 웹 애플리케이션에서 HTTP요청을 처리한데 쓰인다. 나는 이걸 사용할 것이다. 

이 라이브러리의 특징은 promise 기반으로 처리한다는 점이다. 
//promis: 콜백 지옥 같은 코드가 형성되지 않게 하는 방안으로 도입된 기능으로 여러작업을 연달아 처리 한다 해서 함수를 여러번 감싸는 것이 아닌 then을 사용하여 그 다음 작업을 설정한다. 

일단 가짜 api를 호출하여 이에 대한 응답을 보여주는 예제를 실행해 보았다. 




