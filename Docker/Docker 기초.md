TIL 9.17
Docker
리눅스 컨테이너(Linux Container) 기술을 기반으로 하는 오픈 소스 서비스

Linux Container
Linux 기반의 기술 중 하나로, 필요한 라이브러리와 애플리케이션을 모아서 마치 별도의 서버처럼 구성한 것

도커와 가상 머신의 차이
도커는 가상 머신만큼 견고한 격리성을 제공하지는 않습니다.

도커는 리눅스의 컨테이너(Linux Container)를 이용한 기술로, OS 위에 다른 OS를 실행하는 것이 아니므로 가상 머신보다 좋은 성능을 낼 수 있습니다.

애플리케이션에 대한 환경 격리성을 중심으로 한 VM과는 달리, 도커는 Container의 관점에서 개발자와 사용자 커뮤니티를 중심으로 혜택을 제공하는 데 있습니다.

도커 이용하기
레지스트리(Registry)
Docker Hub : https://hub.docker.com/
도커 이미지를 관리하는 공간입니다.
특별히 다른 것을 지정하지 않는다면, 도커 허브(Docker Hub)를 기본 레지스트리로 설정합니다.
레포지토리(Repository)
레지스트리 내에 도커 이미지가 저장되는 공간입니다.
태그(Tag)
해당 이미지를 설명하는 버전 정보를 주로 입력합니다.
특별히 다른 것을 지정하지 않는다면 latest 태그를 붙인 이미지를 가져옵니다.
<최신이미지 혹은 레포지토리 받아오기>
$ docker image pull docker/{이미지 또는 레포지토리}

<이미지 리스트 출력>
$ docker image ls

<작성한 컨테이너 이름으로 컨테이너 이름 생성>
docker container run --name container_name docker/{이미지:latest} cowsay boo

<모든 컨테이너의 리스트를 출력>
docker container ps -a

<이미지 삭제>
docker image rm docker/whalesay

