멘트 없이 코딩화면 공유합니다.
가요를 틀고 싶지만, 저작권 때문에 유튜브 공인 음악만 나오는 점 양해 바랍니다.

https://mp4.okdevtv.com 의 관리자 기능 추가입니다.

일단 로컬의 DB를 update 하겠습니다.

cron 폴더의 script는 1시간씩 돌아가게 만들었습니다.

왼쪽에 슬라이딩 메뉴 섹션을 추가하려고 합니다.

`npx ai-digest`
로 admin 폴더의 파일을 묶어서 하나의 파일로 만듭니다.
codebase.md 파일이 생겼습니다.

이게 이렇게 쉽게 됩니다.
코드 리팩터링(정리 깔끔)을 하고 커밋하겠습니다.

프로젝트도 Kanban 으로 생성해서 구성했습니다.

OKdevTV discord 링크입니다. 
https://discord.gg/3cxND9qJ

odevtuve 는 여기까지입니다.

---
## Google Cloud Platform GCP
GCP 연구하러 이동합니다.
https://console.cloud.google.com

**10분 정도 쉬었다가 00:30에 시작하겠습니다.**
**궁금하신 것은 채팅창에 올려주세요.**

대학교 때 5호관에서 6호관까지 10분안에 이동하려면,
헉헉 댔던 기억이 나네요.

GCP 시작하겠습니다.
appengine 부터 오래 썼는데, aws의 EC2 인스턴스는 많이 사용하지
않아서 연습하려고 합니다.
gmail 계정으로 처음에는 90일간 $300의 크레딧도 제공합니다.
약 41만원 정도 됩니다.

어제 ₩25 / ₩415,288 크레딧 사용됨
25원 썼네요. 😅

VM 만들기
Compute Engine
⬆️ 이게 EC2 같은 것입니다.

서울은 저탄소 Farm이 아니라서 $4 정도 더 비쌉니다.
저탄소 리전은 아이콘이 오른쪽에 있습니다.
일단 진행합니다.

node.js 설치하고, https://okdevtv.com 배포해 보겠습니다.
node.js는 java와 다르게 메모리1G면 충분합니다.
월별 예상 가격
US$9.14

실화냐! 😱

HTTP, HTTPS 까지 도전해 보겠습니다.

일단 ssh는 브라우저에서 합니다.
처음에는 그게 편합니다.

SSH를 클릭합니다.
echo $0 로 bash, zsh을 확인합니다.

zsh을 설치하겠습니다.
https://okdevtv.com/mib/zsh

GCP는 기본이 Debian 계열이라 yum, dnf 아니고,
apt 입니다.

```sh
sudo apt install zsh git htop
sh -c "$(curl -fsSL https://raw.github.com/robbyrussell/oh-my-zsh/master/tools/install.sh)"

```

plugin 없으면 zsh도 심심합니다.

```sh
cd ~/.oh-my-zsh/custom/plugins
git clone https://github.com/zsh-users/zsh-autosuggestions.git
git clone https://github.com/zsh-users/zsh-syntax-highlighting.git

```

```sh
uname -a
```

서버의 종류를 확인하는 법입니다.
x86이네요

du -h 보다 dust를 좋아합니다.
aarch64는 ARM 계열입니다.
지금은 x86으로 설치합니다.

dust 명령은 어느 폴더에 용량이 큰 지 확인하기 아주 좋은 명령어입니다.

node.js 설치를 위한 nvm 차례입니다.
```sh
# node
curl -o- https://raw.githubusercontent.com/nvm-sh/nvm/v0.39.7/install.sh | bash
. ~/.zshrc

```

npm 보다 빠른 pnpm 을 설치하겠습니다.
```sh
npm i -g pnpm
pnpm setup
```


okdevtv 소스를 clone 합니다.

```sh
take ~/git
git clone https://github.com/kenu/okdevtv

```

```sh
cd okdevtv
pnpm i
pnpm dev

```

일단 방화벽을 열고 3000 포트, 인스턴스와 연결하겠습니다.

firewall 연결하느라 땀 2방울 흘렸습니다. 😅

nginx 설치하고, 도메인도 연결해 보겠습니다.
gcp.okdevtv.com

컨닝 조금 하겠습니다.

이건 시간이 좀 걸릴 것 같습니다.

to be continued...
다음 시간에 
つづく

좋은 밤 되시길 바랍니다.
시청 감사합니다. 🙇🏻‍♂️
