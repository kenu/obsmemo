서버를 옮기는 과정에 뭔가 누락된 것 같아서 동작을 안하는 기능입니다.
고치려고 합니다.
Key 이슈였네요. ^^;
오 됩니다. 😀
서버의 키를 수정해야겠습니다.

서버 배포 오늘따라 맘대로 안되네요 ㅠㅠ

1. env key check
2. test case check

create database youtubedb default character set utf8mb4 collate utf8mb4_unicode_ci;
GRANT ALL PRIVILEGES ON *.* TO devuser@localhost IDENTIFIED BY 'devpass' WITH GRANT OPTION;
