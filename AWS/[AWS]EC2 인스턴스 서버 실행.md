EC2 인스턴스에 처음 접속하면 서버를 구동하는 데 필요한 개발 환경을 구축해야 합니다.
패키지 매니저가 관리하는 패키지의 정보를 최신 상태로 업데이트하기 위해서 아래 명령어를 사용합니다.
```
$ sudo apt update
```

아래의 명령어로 nvm, node.js를 설치해야 합니다.
```
$ curl -o- https://raw.githubusercontent.com/nvm-sh/nvm/v0.39.0/install.sh | bash
$ export NVM_DIR="([−z"{XDG_CONFIG_HOME-}" ] && printf %s "HOME/.nvm"∣∣printf{XDG_CONFIG_HOME}/nvm")"
[ -s "$NVM_DIR/nvm.sh" ] && . "$NVM_DIR/nvm.sh" # This loads nvm
$ nvm install node
$ nvm --version (설치가 완료되면 해당 명령어를 이용하여 확인합니다.)
```
nvm설치 참고: https://github.com/nvm-sh/nvm
node.js의 설치가 끝나면 npm 명령어가 정상적으로 입력되지 않는 상황을 방지하기 위해 아래 명령어 입력합니다.
```
$ sudo apt install npm
```
git clone을 이용해 레포지토리를 받고 github ID와 github에서 발급 받은 accessToken을 입력합니다.
```
$ git clone 레포지토리 주소 복사
```
Cloning into '레포지토리'...
Username for 'https://github.com': github ID
Password for 'https://kimcoding@github.com: 발급 받은 accessToken

인스턴스 상 레포지토리 폴더로 이동 후 npm install 명령어를 입력해서 필요한 모듈을 다운 받습니다.
```
$ npm install
```
서버를 실행하지만 에러메시지가 출력됩니다.
```
$ npm start
```
서버를 실행하려면 관리자 권한이 필요하기 때문에 관리자 권한으로 서버를 시작하기 위해서는 sudo npm start 명령어를 입력해야 합니다.
```
$ sudo npm start
```
AWS홈페이지 EC2에서 퍼블릭IPv4를 이용해 홈페이지에 접속합니다.
아마 보안 그룹이 설정되어 있지 않다면 페이지가 정상적으로 rendering 되지 않을 것 입니다.
