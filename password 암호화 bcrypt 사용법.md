bcrypt 사용법
bcrypt 설치

npm install bcrypt
에러 발생시

npm install -g node-gyp
npm install --g --production windows-build-tools
npm install bcrypt
코드 최상단 작성

const bcrypt = require('bcrypt');
bcrypt 사용 코드 예시

 bcrypt.genSalt(10, (err, salt) => {
 	bcrypt.hash(password, salt, async (err, hash) => {
          if(err) {
              throw err;
          } else {
              await users.create({
                  email,
                  nickname,
                  password: hash,
                  user_picture,
                  socialtype
              })
            res.status(201).json({message: "회원가입에 성공하였습니다."});
          }
      })
  })
데이터베이스 암호화(password) 저장
<img width="402" alt="스크린샷 2021-12-26 오후 11 18 40" src="https://user-images.githubusercontent.com/85854164/147411011-37e3d768-7d1a-4d8c-878d-1f735b54815c.png">
