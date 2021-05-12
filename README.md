<h1> 1. 트래픽 </h1>

서버에서 동작하는 서비스에 클라이언트가 접속하여 발생되는 데이터의 전송 수치 즉 서버에 접속량이 많이 늘어남에 따라 트래픽이라는것은 증가하게 된다.

만약 1MB 파일을 10명이 하루에 한번씩 다운받을 경우 10MB로 계산되며 일일 전송 데이터수치인 100MB 트래픽이 발생되었다고 계산할 수 있다.

트래픽 양이 지나치게 늘어나게 되면 서버에서는 그만큼 처리해야할 동작이 많아지므로 서버에 과부하가 걸리게 되고, 서버가 느려지게 된다.
시스템을 안정적으로 기능에 장애가 없이 관리하기 위해서는 서버에서의 트래픽을 관리하고, 또한 서버가 느려짐으로써 다른 클라이언트의 요청이 빠르게 처리되지 않아 유입이 줄어들 수 있다.

이를 관리하기 위해서는 트래픽 기록 현황을 파악하고, 썸네일 같은 이미지들은 리사이징을 통해 관리하는 것이 좋다.


<h1> 2. HTTP와 HTTPS </h1>

HTTP는 하이퍼 텍스트 전송 프로토콜(Hypertext Transfer Protocol)의 약자이다. 서로 다른 시스템들 사이에서 통신을 주고받게 해주는 가장 기초적인 프로토콜, 서버와 클라이언트 사이에 이루어지는 요청과 응답

HTTPS는 하이퍼 텍스트 전송 프로토콜 보안 (Hypertext Transfer Protocol Secure)의 약자. 일반 HTTP와는 다르게 서버에서부터 브라우저로 전송되는 정보가 암호화되지 않지만, SSL을 사용함으로써 정보를 주고 받을 때 도난 당하는 것을 막아줌

* SSL :
