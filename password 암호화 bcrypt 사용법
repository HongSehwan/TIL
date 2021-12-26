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
데이터베이스 암호화(password) 저장 예시

$2b$10$NJ0ZQ5ZDHFpxB2y4LAsrH.FOr6FIilYBe7z2DqXtf9lTg35ahzZcD
$2b$10$OJbOLa6sp3TQ0HXnPN2x6.hrvQHVhqE5KVoLjycIlArIbDgWUWLab
