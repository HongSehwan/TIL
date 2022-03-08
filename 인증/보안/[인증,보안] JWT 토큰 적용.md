JWT 토큰
JWT(Json Web Token)란 Json 포맷을 이용하여 사용자에 대한 속성을 저장하는 Claim 기반의 Web Token이다.
토큰은 세션과 달리 서버가 아닌 클라이언트에 토큰이 저장되어 서버에 부담을 덜수 있다. 토큰 자체에 사용자에 대한 권한 정보나 서비스 사용을 위한 정보가 포함되어 있다.
출처: http://www.opennaru.com/opennaru-blog/jwt-json-web-token/

<JWT 구조>
JWT 토큰은 header, payload, signature 3가지로 구분한다.

header: 토큰의 종류, 암호화 할 알고리즘의 종류가 적혀있다.
{
  "alg": "HS256",
  "typ": "JWT"
}
payload: 어떤 정보에 접근 가능한지에 대한 권한을 담을 수도 있고, 사용자의 유저 이름 등 필요한 데이터는 이곳에 담아 암호화 시켜 담는다. 물론 비밀번호와 같은 민감한 정보는 담지 않는다.
{
  "sub": "someInformation",
  "name": "phillip",
  "iat": 151623391
}
signature: 비밀 키(암호화에 추가할 salt)를 사용하여 암호화합니다.
HMACSHA256(base64UrlEncode(header) + '.' + base64UrlEncode(payload), secret);
JWT의 종류
Access Token: Access token은 보호된 정보들(유저의 이메일, 연락처, 사진 등)에 접근할 수 있는 권한부여에 사용한다. 유효기간 설정은 되도록 짧게 설정한다.

Refresh Token: Access token의 유효기간이 만료된다면 refresh token을 사용하여 새로운 access token을 발급 받을 수 있다. 당연히 Access token보다 유효기간을 길게 설정해야 하며

토큰 인증 절차
클라이언트가 서버에 아이디/비밀번호를 담아 로그인 요청을 보낸다.
아이디/비밀번호가 일치하는지 확인하고, 클라이언트에게 보낼 암호화된 access/refresh 토큰을 생성한다.
토큰을 클라이언트에게 보내주면, 클라이언트는 토큰을 저장한다.
(저장하는 위치는 local storage, cookie, react의 state 등 다양하다.)
클라이언트가 HTTP 헤더(authorization 헤더)에 토큰을 담아 보낸다.
서버는 토큰을 해독하여 토큰 확인이 될 경우, 클라이언트의 요청을 처리한 후 응답을 보내준다.
출처: https://m.blog.naver.com/shino1025/221568544633
