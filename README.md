<h1> 1. 트래픽 </h1>

서버에서 동작하는 서비스에 클라이언트가 접속하여 발생되는 데이터의 전송 수치 즉 서버에 접속량이 많이 늘어남에 따라 트래픽이라는것은 증가하게 된다.

만약 1MB 파일을 10명이 하루에 한번씩 다운받을 경우 10MB로 계산되며 일일 전송 데이터수치인 100MB 트래픽이 발생되었다고 계산할 수 있다.

트래픽 양이 지나치게 늘어나게 되면 서버에서는 그만큼 처리해야할 동작이 많아지므로 서버에 과부하가 걸리게 되고, 서버가 느려지게 된다.
시스템을 안정적으로 기능에 장애가 없이 관리하기 위해서는 서버에서의 트래픽을 관리하고, 또한 서버가 느려짐으로써 다른 클라이언트의 요청이 빠르게 처리되지 않아 유입이 줄어들 수 있다.

이를 관리하기 위해서는 트래픽 기록 현황을 파악하고, 썸네일 같은 이미지들은 리사이징을 통해 관리하는 것이 좋다.


<h1> 2. HTTP와 HTTPS </h1>

HTTP는 하이퍼 텍스트 전송 프로토콜(Hypertext Transfer Protocol)의 약자이다. 서로 다른 시스템들 사이에서 통신을 주고받게 해주는 가장 기초적인 프로토콜, 서버와 클라이언트 사이에 이루어지는 요청과 응답 하지만 HTTP는 암호화가 되지 않은 평문 데이터를 전송하는 프로토콜이였기 때문에, HTTP로 비밀번호나 주민등록번호 등을 주고 받으면 제3자가 정보를 조회할 수 있었다. 그리고 이러한 문제를 해결하기 위해 HTTPS가 등장하게 되었다.

HTTPS는 하이퍼 텍스트 전송 프로토콜 보안 (Hypertext Transfer Protocol Secure)의 약자. HTTP에 데이터 암호화가 추가된 프로토콜이다. 네트워크 상에서 중간에 제3자가 정보를 볼 수 없도록 공개키 암호화를 지원하고 있다.

[HTTPS 동작 과정]
1) A기업은 HTTP 기반의 애플리케이션에 HTTPS를 적용하기 위해 공개키/개인키 발급
2) CA 기업에게 돈을 지불하고, 공개키를 저장하는 인증서의 발급을 요청
3) CA 기업은 CA기업의 이름, 서버의 공개키, 서버의 정보 등을 기반으로 인증서를 생성하고, CA 기업의 개인키로 암호화하여 A기업에게 이를 제공
4) A기업은 클라이언트에게 암호화된 인증서를 제공함.
5) 브라우저는 CA기업의 공개키를 미리 다운받아 갖고 있어, 암호화된 인증서를 복호화 함
6) 암호화된 인증서를 복호화하여 얻은 A기업의 공개키로 데이터를 암호화하여 요청을 전송함


<img src="https://user-images.githubusercontent.com/60728267/118079270-d6ac3680-b3f2-11eb-83fd-91701470a789.png">

<h1> 3. 크로스 브라우징 </h1>

크로스 브라우징은 W3C에서 채택된 표준 웹 기술을 적용해 모든 브라우저에 다른 기종의 OS나 HTML 렌더링 기술로
비슷하게 만들어 어떤 환경에서도 이상없이 작동되게 하는 웹페이지를 제작하는 방법론이다.

대체로 모든 브라우저에서 똑같이 보이게 하는 것으로 알고 있지만 이는 잘못된 의미이다.

크로스 브라우징은 동일성이 아닌 동등성을 의미한다.

크로스 브라우징이란 표준 웹 기술을 적용하여 다른 기종 혹은 플랫폼에 따라 달리 구현되는 기술을 비슷하게 만듦과 동시에 어느 한쪽에 최적화되어 치우치지 않고 공통 요소를 사용하여 웹 페이지를 제작하는 기법을 말함

<h1> 3. MVC 패턴</h1>

관심사를 모델, 뷰, 컨트롤러의 세 가지 구성 요소로 나누는 설계 패턴

모델 : 컨트롤러에 의해 호출되어 데이터소스에 데이터를 저장하거나 데이터를 가져와서 뷰가 사용할 수 있는 형태로 컨트롤러에 반환
뷰 : 컨트롤러에 의해 호출되어 클라이언트에게 응답할 내용을 생성해서 컨트롤러에 반환
컨트롤러 : 사용자의 요청을 처리하고 응답을 되돌려주는 전체 과정을 관장
- 세션 시작 및 의존패키지를 로드하는 등 애플리케이션이 요청을 처리하는데 필요한 기본적인 작업을 수행
- 사용자가 입력한 데이터를 검증
- 모델을 호출하여 데이터소스와 관련된 일을 처리
- 뷰를 호출하여 응답을 생성
- 뷰가 생성한 응답을 클라이언트에게 전달

장점 : 관심사 분리에 따른 장점. 개별 부문을 이해하기 쉬워지고 각 부문 재사용, 유지보수와 협업이 쉬워짐


<h1> 4. 프런트 컨틀롤러 패턴</h1>

웹 애플리케이션으로 오는 모든 리소스 요청을 처리해주는 하나의 진입점(index.php)을 두는 패턴

장점
1) 모든 요청에 대해 항상 수행해야 하는 작업을 한 곳에서 수행할 수 있다.
2) URL을 더 의미 있게 제공할 수 있다.
3) 파일 구조가 바뀌어도 URL을 유지할 수 있다.
4) 보안성이 강화된다.

<h1> 5. OOP</h1>
OOP(Object-Oriented Programming)란 객체와 객체의 유기적인 상호작용을 통해 프로그램이 동작하는 것이며, 하나의 클래스를 바탕으로 서로 다른 인스턴스를 만들면서 다른 행동들을 하게 할 수 있다.

장점 : 코드 재사용, 유지 보수 

