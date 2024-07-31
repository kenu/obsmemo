

2. 
3. **기초 지식 및 CI의 중요성 (30분)**
    - 소프트웨어 개발 생명주기의 개요
    - 버그 발견 및 수정 과정에서의 문제점
    - CI가 제공하는 이점: 빠른 피드백, 자동화된 테스트, 코드 품질 향상

4. **CI의 정의 및 원리 (45분)**
    - CI의 정의: 지속적인 통합
    - CI의 목적: 코드의 통합과 테스트를 자동화하여 소프트웨어 개발 프로세스를 가속화하고 안정성을 높이는 것
    - CI 파이프라인의 구성 요소: 소스 컨트롤, 빌드 시스템, 테스트 프레임워크, 배포 도구
    - CI 파이프라인의 작동 방식: 코드 변경 시 자동으로 빌드 및 테스트 실행

5. **CI 도구 및 플랫폼 소개 (60분)**
    - 주요 CI 도구: Jenkins, GitLab CI, CircleCI, GitHub Actions
    - 각 도구의 특징 및 사용 사례
    - CI 파이프라인 구축 예시: Jenkinsfile 작성, GitHub Actions YAML 파일 설정
    - CI 파이프라인의 예시: 자동 빌드, 단위 테스트, 통합 테스트, 배포 스크립트 실행
zstd
https://github.com/facebook/zstd/releases/download/v1.5.6/zstd-v1.5.6-win64.zip




https://docs.aws.amazon.com/ko_kr/AWSEC2/latest/UserGuide/add-instance-store-volumes.html
https://docs.aws.amazon.com/ebs/latest/userguide/ebs-using-volumes.html#ebs-mount-after-reboot


https://github.com/bootandy/dust/releases

https://github.com/bootandy/dust/releases/download/v1.0.0/dust-v1.0.0-x86_64-unknown-linux-gnu.tar.gz

```
(base) ➜  / dust 
Did not have permissions for all directories
1.2G   ┌── data                   │███                                    │   7%
985M   │ ┌── lib                  │███░░░░░░                              │   6%
1.0G   │ ├── lib64                │███░░░░░░                              │   6%
3.8G   ├─┴ usr                    │█████████                              │  22%
935M   │         ┌── 6            │███▓▓▓▓▓▓▒▒▒▒▒▒▒▒▒▒▒▒▒▒▒▒▒             │   5%
1.1G   │         ├── 3            │███▓▓▓▓▓▓▒▒▒▒▒▒▒▒▒▒▒▒▒▒▒▒▒             │   6%
3.2G   │       ┌─┴ http-v2        │███████▓▓▒▒▒▒▒▒▒▒▒▒▒▒▒▒▒▒▒             │  18%
3.2G   │     ┌─┴ pip              │███████▓▓▒▒▒▒▒▒▒▒▒▒▒▒▒▒▒▒▒             │  18%
4.0G   │   ┌─┴ .cache             │█████████▒▒▒▒▒▒▒▒▒▒▒▒▒▒▒▒▒             │  23%
1.4G   │   │         ┌── lib      │████▓▓▓▓▓▓▓▓▓▓▓▓▒▒▒▒▒▒▒▒▒▒             │   8%
1.5G   │   │       ┌─┴ torch      │████▓▓▓▓▓▓▓▓▓▓▓▓▒▒▒▒▒▒▒▒▒▒             │   9%
1.1G   │   │       │   ┌── lib    │███▓▓▓▓▓▓▓▓▓▓▓▓▓▒▒▒▒▒▒▒▒▒▒             │   6%
1.1G   │   │       │ ┌─┴ cudnn    │███▓▓▓▓▓▓▓▓▓▓▓▓▓▒▒▒▒▒▒▒▒▒▒             │   6%
2.8G   │   │       ├─┴ nvidia     │███████▓▓▓▓▓▓▓▓▓▒▒▒▒▒▒▒▒▒▒             │  16%
6.4G   │   │     ┌─┴ site-packages│███████████████▓▒▒▒▒▒▒▒▒▒▒             │  37%
6.4G   │   │   ┌─┴ python3.10     │███████████████▓▒▒▒▒▒▒▒▒▒▒             │  37%
6.6G   │   │ ┌─┴ lib              │███████████████▓▒▒▒▒▒▒▒▒▒▒             │  38%
7.2G   │   ├─┴ miniconda3         │████████████████▒▒▒▒▒▒▒▒▒▒             │  42%
 11G   │ ┌─┴ ec2-user             │██████████████████████████             │  66%
 11G   ├─┴ home                   │██████████████████████████             │  66%
 17G ┌─┴ .                        │██████████████████████████████████████ │ 100%
(base) ➜  / 

```

mkdir ~/app/.cache ~/app/git ~/app/miniconda3
ln -s ~/app/.cache ~/.cache
ln -s ~/app/git ~/git      
ln -s ~/app/miniconda3 ~/miniconda3


mkdir -p ~/miniconda3
wget https://repo.anaconda.com/miniconda/Miniconda3-latest-Linux-x86_64.sh -O ~/miniconda3/miniconda.sh
bash ~/miniconda3/miniconda.sh -b -u -p ~/miniconda3
rm -rf ~/miniconda3/miniconda.sh
~/miniconda3/bin/conda init zsh
. ~/.zshrc
conda install python=3.8.5




https://docs.aws.amazon.com/ko_kr/AWSEC2/latest/UserGuide/install-nvidia-driver.html

sudo snap install aws-cli --classic


Please make sure that

 -   PATH includes /usr/local/cuda-12.5/bin

 -   LD_LIBRARY_PATH includes /usr/local/cuda-12.5/lib64, or, add /usr/local/cuda-12.5/lib64 to /etc/ld.so.conf and run ldconfig as root


sudo sh downloaded_installer_file --silent --override --toolkit --samples --toolkitpath=/usr/local/cuda-12.5 --samplespath=/usr/local/cuda --no-opengl-libs

sudo ln -s /usr/local/cuda-12.5 /usr/local/cuda


mkdir -p ~/miniconda3
wget https://repo.anaconda.com/miniconda/Miniconda3-latest-Linux-x86_64.sh -O ~/miniconda3/miniconda.sh
bash ~/miniconda3/miniconda.sh -b -u -p ~/miniconda3
rm -rf ~/miniconda3/miniconda.sh
~/miniconda3/bin/conda init zsh
. ~/.zshrc
conda install python=3.8.5

conda activate tooncrafter

`g4dn.2xlarge`
torch.cuda.OutOfMemoryError: CUDA out of memory. Tried to allocate 1.25 GiB (GPU 0; 14.74 GiB total capacity; 13.69 GiB already allocated; 62.12 MiB free; 14.53 GiB reserved in total by PyTorch) If reserved memory is >> allocated memory try setting max_split_size_mb to avoid fragmentation.  See documentation for Memory Management and PYTORCH_CUDA_ALLOC_CONF

```
1  cd ~/.oh-my-zsh/custom/plugins\ngit clone https://github.com/zsh-users/zsh-autosuggestions.git\ngit clone https://github.com/zsh-users/zsh-syntax-highlighting.git\n

    2  vi ~/.zshrc\n

    3  # node\ncurl -o- https://raw.githubusercontent.com/nvm-sh/nvm/v0.39.7/install.sh | bash\n. ~/.zshrc\n

    4  docker compose version

    5  df -h\nlsblk\nsudo mkfs -t xfs /dev/nvme1n1\nsudo mkdir /data\nsudo mount /dev/nvme1n1 /data\n# mount after reboot\nln -s /data ~/app\ncd ~/app\nsudo chown ec2-user:ec2-user .\ntouch hello\ncd /data\nls -altr\n

    6  mkdir -p ~/app/.cache ~/app/git ~/app/miniconda3\nln -s ~/app/.cache ~/.cache\nln -s ~/app/git ~/git\nln -s ~/app/miniconda3 ~/miniconda3\n

    7  cd ~/app

    8  ls -altr

    9  ls -al ~

   10  sudo chown ubuntu:ubuntu .

   11  touch hello

   12  cd /data

   13  ls -altr

   14  aws 

   15  history

   16  sudo apt install aws

   17  sudo apt install awscli

   18  sudo apt install aws-cli

   19  snap install aws-cli

   20  sudo snap install aws-cli

   21  sudo snap install aws-cli --classic

   22  aws configure

   23  df -h

   24  sudo mount /dev/nvme1n1 /data

   25  df -h

   26  sudo apt-get install -y gcc make linux-headers-$(uname -r)

   27  cat << EOF | sudo tee --append /etc/modprobe.d/blacklist.conf\nblacklist vga16fb\nblacklist nouveau\nblacklist rivafb\nblacklist nvidiafb\nblacklist rivatv\nEOF

   28  ls -l /etc/default/grub

   29  sudo vi /etc/default/grub

   30  sudo update-grub

   31  aws s3 cp --recursive s3://ec2-linux-nvidia-drivers/latest/ .

   32  aws s3 ls --recursive s3://ec2-linux-nvidia-drivers/

   33  chmod +x NVIDIA-Linux-x86_64*.run

   34  ls -altr

   35  sudo /bin/sh ./NVIDIA-Linux-x86_64*.run

   36  nvidia-smi -q | head

   37  sudo touch /etc/modprobe.d/nvidia.conf

   38  echo "options nvidia NVreg_EnableGpuFirmware=0" | sudo tee --append /etc/modprobe.d/nvidia.conf

   39  sudo reboot

   40  sudo mount /dev/nvme1n1 /data

   41  df -h

   42  cat /etc/issue

   43  wget https://developer.download.nvidia.com/compute/cuda/12.5.0/local_installers/cuda_12.5.0_555.42.02_linux.run

   44  sudo sh cuda_12.5.0_555.42.02_linux.run

   45  df -h

   46  htop

   47  cat /var/log/cuda-installer.log

   48  sudo sh cuda_12.5.0_555.42.02_linux.run

   49  echo $LD_LIBRARY_PATH

   50  vi ~/.zshrc\n

   51  . ~/.zshrc

   52  sudo ldconfig

   53  sudo ln -s /usr/local/cuda-12.5 /usr/local/cuda

   54  ls -al /usr/local/cuda

   55  cd /usr/local/cuda

   56  ls -altr

   57  conda create -n tooncrafter python=3.8.5

   58  mkdir -p ~/miniconda3\nwget https://repo.anaconda.com/miniconda/Miniconda3-latest-Linux-x86_64.sh -O ~/miniconda3/miniconda.sh\nbash ~/miniconda3/miniconda.sh -b -u -p ~/miniconda3\nrm -rf ~/miniconda3/miniconda.sh\n~/miniconda3/bin/conda init zsh\n. ~/.zshrc\nconda install python=3.8.5

   59  conda activate tooncrafter

   60  cd ~/git

   61  git clone https://github.com/ToonCrafter/ToonCrafter

   62  cd ToonCrafter

   63  conda activate tooncrafter

   64  conda create -n tooncrafter python=3.8.5\n

   65  conda activate tooncrafter

   66  pip install -r requirements.txt

   67  sh scripts/run.sh

   68  df -h

   69  sh scripts/run.sh

   70  python gradio_app.py 

   71  df -h

   72  curl http://127.0.0.1:7860

   73  vi gradio_app.py

   74  python gradio_app.py
```


```
df -h
lsblk
sudo mkfs -t xfs /dev/nvme1n1
sudo mkdir /data
sudo mount /dev/nvme1n1 /data
# mount after reboot
ln -s /data ~/app
cd ~/app
sudo chown ubuntu:ubuntu .
touch hello
cd /data
ls -altr

```

https://github.com/ToonCrafter/ToonCrafter


```
[Unit]
Description=yona
After=syslog.target network.target

[Service]
User=ec2-user
Group=ec2-user

ExecStart=/home/ec2-user/local/reyona.sh
ExecStop=/bin/kill -15 $MAINPID
SuccessExitStatus=143

[Install]
WantedBy=multi-user.target
```

- `vi ~/local/reyona.sh`
```
#!/usr/bin/zsh
HOME=/home/ec2-user
source $HOME/.zshrc

test -f $HOME/local/yona/RUNNING_PID && rm -f $HOME/local/yona/RUNNING_PID

nohup $HOME/local/yona/bin/yona&
```

- `chmod +x ~/local/reyona.sh`
- `~/local/reyona.sh`

https://okdevtv.com/mib/yona

1. ec2 instance
2. install mariadb105
3. install java11, not 17



```
~~~~~~
* VS Code로 쉽게 시작하는 Git, GitHub
  * 인프런: https://inf.run/LPpDg
* React + API Server 프로젝트 개발과 배포 #CI/CD
  * https://bit.ly/oklearnreact
```


https://archive.org/details/WindowsXPProfessionalKwithServicePack3Korean
