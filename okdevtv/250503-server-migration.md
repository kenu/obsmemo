2 small 인스턴스를 1 medium 인스턴스로 통합


- [x] https://okdevtv.com
- [x] https://mp4.okdevtv.com
- [x] https://yona.okdevtv.com
- [x] https://10y.okdevtv.com


2 cpu 4G ram
t4g.medium
$0.0416 / hour
0.0416 * 24 * 31 * 1400
43330.56원 / month

US$0.0252 # 1년약정 60%
US$0.0289
US$0.0180 # 3년약정 40%
US$0.0211


1. okdevtv.com
2. mp4.okdevtv.com
3. 10y.okdevtv.com

- [x] 운영환경 세팅
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

```
[mariadb]
lower_case_table_names=1
```

- [x] nginx 설치
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

- [x] new.okdevtv.com 도메인 설정
- https://www.cloudflare.com
- https://okdevtv.com/mib/letsencrypt #deprecated

- [x] 환경변수
	- `env` 
	- API_KEY, DB정보, 등


- [x] scripts 이전
- `scripts/` folder

- [x] crontab
- https://felo.ai/search/mGxnuvpY4FPnSKKjve8URs?invite=B8oRvQ3gJWyK0
```
sudo dnf install cronie -y
sudo systemctl start crond
crontab -e
```

```sh
5 0,2,8-23 * * * /home/ec2-user/scripts/cron-video.sh >> /tmp/cronyou.log
```


```
server {
    server_name  www.okdevtv.com;
    rewrite ^(.*) http://okdevtv.com$1 permanent;
}

```



```
server {
    server_name  www.okdevtv.com;
    rewrite ^(.*) https://okdevtv.com$1 permanent;



    listen 443 ssl; # managed by Certbot
    ssl_certificate /etc/letsencrypt/live/www.okdevtv.com/fullchain.pem; # managed by Certbot
    ssl_certificate_key /etc/letsencrypt/live/www.okdevtv.com/privkey.pem; # managed by Certbot
    include /etc/letsencrypt/options-ssl-nginx.conf; # managed by Certbot
    ssl_dhparam /etc/letsencrypt/ssl-dhparams.pem; # managed by Certbot




}

server {
    server_name  okdevtv.com; # managed by Certbot

    # Load configuration files for the default server block.
    include /etc/nginx/default.d/*.conf;

    location / {
        sendfile off;
        proxy_pass         http://127.0.0.1:3000;
        proxy_redirect     default;
        proxy_http_version 1.1;
        proxy_set_header   Host              $host;
        proxy_set_header   X-Real-IP         $remote_addr;
        proxy_set_header   X-Forwarded-For   $proxy_add_x_forwarded_for;
        proxy_set_header   X-Forwarded-Proto $scheme;
        proxy_cache_bypass $http_upgrade;
        proxy_max_temp_file_size 0;
    }

    error_page 404 /404.html;
        location = /40x.html {
    }

    error_page 500 502 503 504 /50x.html;
        location = /50x.html {
    }




    listen 443 ssl; # managed by Certbot
    ssl_certificate /etc/letsencrypt/live/okdevtv.com-0001/fullchain.pem; # managed by Certbot
    ssl_certificate_key /etc/letsencrypt/live/okdevtv.com-0001/privkey.pem; # managed by Certbot
    include /etc/letsencrypt/options-ssl-nginx.conf; # managed by Certbot
    ssl_dhparam /etc/letsencrypt/ssl-dhparams.pem; # managed by Certbot




}


server {
    if ($host = okdevtv.com) {
        return 301 https://$host$request_uri;
    } # managed by Certbot


    server_name  okdevtv.com;
    listen 80;
    return 404; # managed by Certbot


}
server {
    if ($host = www.okdevtv.com) {
        return 301 https://$host$request_uri;
    }

    server_name  www.okdevtv.com;
    listen 80;
    return 404;
}
```