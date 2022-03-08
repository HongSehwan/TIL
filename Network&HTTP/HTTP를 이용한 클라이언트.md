TIL - 07.29
HTTP를 이용한 클라이언트
클라이언트 서버 아키텍처(2-Tier 아키텍처)
리소스가 존재하는곳(서버)과 리소스를 사용하는앱(클라이언트)
을 분리시킨 것.

3-Tier 아키텍처
클라이언트 - 서버 아키텍처에 데이터베이스가 추가된 형태

프로토콜
프로토콜: 통신규약
(응용계층 주요 프로토콜)
HTTP : 웹에서 HTML, JSON 등의 정보를 주고받는 프로토콜
HTTPS : HTTP보다 보안이 강화 된 프로토콜
FTP : 파일 전송 프로토콜
SMTP : 메일을 전송하기 위한 프로토콜
SSH : CLI환경에서 원격 컴퓨터에 접속하기 위한 프로토콜
RDP : window계열의 원격 컴퓨터에 접속하기 위한 프로토콜
WebSocket : 실시간 통신, Push 등을 지원하는 프로토콜
(전송계층 주요 프로토콜)
TCP : HTTP, FTP 통신 등의 근간이 되는 인터넷 프로토콜
UDP : (양방향의 TCP와는 다르게) 단 방향으로 작동하는 훨씬 더 단순하고 빠르지만 신뢰성이 낮은 인터넷 프로토콜
HTTP 메시지
HTTP라는 프로토콜을 이용해 메시지를 주고 받음.

API(Application Programming Interface)
서버가 클라이언트에게 리소스를 잘 활용할 수 있도록 인터페이스(interface)를 제공
HTTP API 디자인
(HTTP요청 메서드)

- GET : 특정 리소스의 표시를 요청합니다.
- HEAD : GET 메서드의 요청과 동일한 응답을 요구하지만, 
	 응답 본문을 포함하지 않습니다.
- POST : 특정 리소스에 엔티티를 제출할 때 쓰입니다. 
- PATCH : 리소스의 부분만을 수정하는 데 쓰입니다.
- PUT : 목적 리소스 모든 현재 표시를 요청 payload로 바꿉니다.
- DELETE : 특정 리소스를 삭제합니다
- CONNECT : 목적 리소스로 식별되는 서버로의 터널을 맺습니다.
- OPTIONS : 목적 리소스의 통신을 설정하는 데 쓰입니다.
- TRACE : 리소스의 경로를 따라 메시지 loop-back 테스트를 합니다.
URL(Uniform Resource Locator)
네트워크 상에서 웹 페이지, 이미지, 동영상 등의 파일이 위치한 정보를 나타낸다.

scheme : 통신 방식(프로토콜)을 결정
일반적인 웹브라우저에서는 http(s)를 사용
hosts : 웹 서버의 이름이나 도메인, IP를 사용하며 주소를 나타냄.
port : 웹 서버에 접속하기 위한 통로
url-path : 웹 서버에서 지정한 루트 디렉토리부터 시작하여 웹 페이지, 이미지, 동영상 등이 위치한 경로와 파일명을 나타냄.
URI(Uniform Resource Identifier)
URL의 기본 요소인 scheme, hosts, url-path에 더해 query, bookmark를 포함(URL을 포함하는 상위개념)

query : 웹 서버에 보내는 추가적인 질문
