너무 오래 놓아 두었던 에러를 처리하려고 합니다.
https://okdevtv.com 의 로그인 및 회원가입이 전혀 되지 않고 있었습니다.
😅

```
Error: Failed to obtain access token  
    at /home/ec2-user/git/okdevtv/node_modules/.pnpm/passport-oauth2@1.8.0/node_modules/passport-oauth2/lib/strategy.js:178:49  
    at /home/ec2-user/git/okdevtv/node_modules/.pnpm/oauth@0.10.0/node_modules/oauth/lib/oauth2.js:214:7  
    at passBackControl (/home/ec2-user/git/okdevtv/node_modules/.pnpm/oauth@0.10.0/node_modules/oauth/lib/oauth2.js:134:9)  
    at IncomingMessage.<anonymous> (/home/ec2-user/git/okdevtv/node_modules/.pnpm/oauth@0.10.0/node_modules/oauth/lib/oauth2.js:157:7)  
    at IncomingMessage.emit (node:events:531:35)  
    at IncomingMessage.emit (node:domain:488:12)  
    at endReadableNT (node:internal/streams/readable:1696:12)  
    at process.processTicksAndRejections (node:internal/process/task_queues:82:21)
```

에러 메시지에는 스택트레이스라고 해서 Stack Trace(어느 함수가 어떤 함수를 부르는지 다른 말로 Call Stack)가 나와서 당황😱하게 만듭니다.
중요한 것은 핵심 메시지를 찾는 것입니다.

대부분은 첫줄 또는 마지막에 나옵니다.
```
Error: Failed to obtain access token
```

로컬에서도 확인을 해 봐야 할 것 같습니다.
```
git clone https://github.com/kenu/okdevtv
cd okdevtv
pnpm i
pnpm dev
```

일단 로컬에서 사이트는 열렸습니다.
GitHub Login key 설정이 필요합니다.
다른 계정으로 해 보겠습니다. github에 계정이 3개 로그인 되어 있습니다.

GitHub 계정의 Settings로 들어갑니다.
https://github.com/settings/profile
왼쪽 메뉴 마지막에 Developer settings 메뉴로 들어갑니다.
https://github.com/settings/apps
OAuth과 로그인과 연관이 있습니다.

새로운 로컬 개발용 키를 생성했습니다.
Ov23liom7nqZjZdMRQjZ
Secret도 필요합니다.
z-f28a8462eaa0b367724

.env.sample 을 .env 로 복사하고 GitHub 부분을 채웁니다.
방송을 마치면 방금 만든 키와 앱은 삭제할 것입니다.
노출되면 집 번호키를 공개한 것과 같은 느낌입니다.😱

서버를 재시작하고, 테스트를 해 보겠습니다.
아, DB가 필요합니다.
로컬의 DB도 지우고 가보겠습니다.
https://okdevtv.com/mib/mariadb 참고하시면 됩니다.

```sql
create database devdb default character set utf8mb4 collate utf8mb4_unicode_ci;

GRANT ALL PRIVILEGES ON devdb.* TO devuser@localhost IDENTIFIED BY 'devpass' WITH GRANT OPTION;
```

로그인 시도를 해 보겠습니다.
login과 signup을 동시에 생각했는데, signup 부분이 이슈인 것 같습니다.

길을 잃었을 때는 다시 돌아가서 하나씩 디버깅해보는 게 상책입니다.
상책아~~~
디버그 모드로 서버를 띄우겠습니다.

```
    sqlMessage: "Access denied for user 'kenu'@'localhost'",
```
이 에러 메시지에서는 핵심 키워드가 
`sqlMessage` 였습니다. DB 접속이 안된다는 뜻입니다.

띠로리 ㅠㅠ 3년 전 제가 밉네요 ㅠㅠ

거의 다 온 것 같습니다.
