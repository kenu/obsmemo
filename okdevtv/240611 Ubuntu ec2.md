Amazon Linux 와 달리 ubuntu OS로 진행해 봅니다.

기본 zsh 로 바꾸고, node.js, java, python 등을 설치해 봅니다.

패키지 매니저가 바뀌는 것이 제일 큰 변화로 생각됩니다.
dnf, yum -> apt(apt-get)

인스턴스 시작하겠습니다.

사용자 이름은 ec2-user가 아닙니다. ubuntu 입니다.

ssh -i ~/keys/okkyelk.pem ubuntu@43.203.226.18


---
sudo dnf install zsh git util-linux-user -y
sudo apt install zsh git -y
sudo apt install zip unzip -y

```sh
sudo groupadd docker
sudo usermod -aG docker ${USER}
sudo reboot
```

ubuntu는 docker compose 설치가 따로 필요 없네요.

sudo snap install dust

오늘은 이 정도로 우분투 테스트를 마치겠습니다.
시청 감사합니다. 🙇‍♂️
