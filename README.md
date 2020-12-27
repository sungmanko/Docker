# Docker
Docker初心者のお勉強用


１．dockerをインストールする
>https://www.docker.com/get-started

＜正しいインストール確認方法＞
cmdを開いて、docker --version を入力してみると
Docker version 20.10.0, build 7287ab3
このようなバージョン情報を確認することが出来る。


２．Oracleインストール
下記のリンクからチェックアウト
>https://hub.docker.com/_/oracle-database-enterprise-edition?tab=resources

※これはDocker加入を行い、個人アカウントのレポジトリを使うことになるので、
・DockerにSignIN
・Oracleへの同意＆プルリンク取得が必要

どうすると、Dockerにログインしておいてから
cmdで下記のコマンドを記入することでプルすることが出来る（2.7gb）
>docker pull store/oracle/database-enterprise:12.2.0.1

インストールが完了すると下記のようになる。（CMD内部）
C:\Users\kangf>docker pull store/oracle/database-enterprise:12.2.0.1
12.2.0.1: Pulling from store/oracle/database-enterprise
4ce27fe12c04: Pull complete                                                                               
9d3556e8e792: Pull complete                                                                               
fc60a1a28025: Pull complete                                                                               
0c32e4ed872e: Pull complete                                                                               
b465d9b6e399: Pull complete                                                                               
Digest: sha256:40760ac70dba2c4c70d0c542e42e082e8b04d9040d91688d63f728af764a2f5d
Status: Downloaded newer image for store/oracle/database-enterprise:12.2.0.1
docker.io/store/oracle/database-enterprise:12.2.0.1

３．ダウンロードしたイメージをコンテナで起動する。（初期1.3gb）
>docker run -dit --name local_db -p 1521:1521 store/oracle/database-enterprise:12.2.0.1-slim

４．Docker起動確認
>docker ps -a

５．A5M2をインストール
>https://a5m2.mmatsubara.com/

６．Oracleを設定してみる



それでは確認作業を行う。
インストール後の基本情報は下記となる
>USER = sys / Oradoc_db1
>DB_SID=ORCLCDB
>DB_PDB=ORCLPDB1
>DB_MEMORY=2GB
>DB_DOMAIN=localdomain

