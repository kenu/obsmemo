https://okdevtv.com
https://mp4.okdevtv.com
https://yona.okdevtv.com
https://10y.okdevtv.com


2 cpu 4G ram
t4g.medium
$0.0416 / hour

1. okdevtv.com
2. mp4.okdevtv.com
3. 10y.okdevtv.com

- [ ] 운영환경 세팅
- https://okdevtv.com/mib/egov/msa
```sh
sudo dnf install zsh git util-linux-user htop -y

sh -c "$(curl -fsSL https://raw.github.com/robbyrussell/oh-my-zsh/master/tools/install.sh)" # oh-my-zsh

```

```sh
cd ~/.oh-my-zsh/custom/plugins
git clone https://github.com/zsh-users/zsh-autosuggestions.git
git clone https://github.com/zsh-users/zsh-syntax-highlighting.git

```

```sh
curl -o- https://raw.githubusercontent.com/nvm-sh/nvm/v0.40.3/install.sh | bash  
. ~/.zshrc
nvm i 22
nvm ls-remote

node -v
```

```sh
curl -s "https://get.sdkman.io" | bash

```


- [x] DB 세팅 MariaDB
https://okdevtv.com/mib/mariadb

```sh
sudo dnf install mariadb105-server -y
sudo systemctl enable mariadb
sudo systemctl start mariadb
sudo mariadb-secure-installation
```

```sh
create database devdb default character set utf8mb4 collate utf8mb4_unicode_ci;
GRANT ALL PRIVILEGES ON devdb.* TO devuser@localhost IDENTIFIED BY 'devpass' WITH GRANT OPTION;
```

- [ ] nginx 설치
- https://okdevtv.com/mib/nginx
```sh
sudo dnf install nginx -y
sudo systemctl enable nginx
```

```sh
sudo su -
cd /etc/nginx
vi nginx.conf

```

- [ ] new.okdevtv.com 도메인 설정
- https://www.cloudflare.com
- 
- [ ] 
