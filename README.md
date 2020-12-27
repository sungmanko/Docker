# Docker
Docker初心者のお勉強用


１．dockerをインストールする
https://www.docker.com/get-started

＜正しいインストール確認方法＞
cmdを開いて、docker --version を入力してみると
Docker version 20.10.0, build 7287ab3
このようなバージョン情報を確認することが出来る。


２．Oracleインストール
下記のリンクからチェックアウト
https://hub.docker.com/_/oracle-database-enterprise-edition?tab=resources

※これはDocker加入を行い、個人アカウントのレポジトリを使うことになるので、
・DockerにSignIN
・Oracleへの同意＆プルリンク取得が必要

どうすると、Dockerにログインしておいてから
cmdで下記のコマンドを記入することでプルすることが出来る（2.7gb）
>docker pull store/oracle/database-enterprise:12.2.0.1




