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



lol champions
https://ddragon.leagueoflegends.com/cdn/img/champion/splash/Aphelios_0.jpg
https://ddragon.leagueoflegends.com/cdn/img/champion/splash/Lillia_0.jpg
https://ddragon.leagueoflegends.com/cdn/img/champion/splash/Samira_0.jpg
https://ddragon.leagueoflegends.com/cdn/img/champion/splash/Seraphine_0.jpg
https://ddragon.leagueoflegends.com/cdn/img/champion/splash/Sett_0.jpg
https://ddragon.leagueoflegends.com/cdn/img/champion/splash/Volibear_0.jpg

https://cmsassets.rgpub.io/sanity/images/dsfx7636/game_data_live/baa25073a0560dbfffa5fafa9eeebe3bd27c4206-496x560.jpg?auto=format&fit=fill&q=80&w=356

http://localhost:8080/worldcup/index.jsp?set=lol
