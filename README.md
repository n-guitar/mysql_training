# mysqlトレーニング用
- てっとりはやくwordpressでDBとテーブルを作成してSQLに触れてみる


# 前提条件
 - 環境はmacとし、brew環境があること。
 - docker for macがあること。
 
 
# 環境構築

## ファイルダウンロード

```bash
$ git clone https://github.com/n-guitar/mysql_training.git
```
 　
## mac用MySqlクライアントインストール

```bash
$ brew install mysql
```
 　

## mac用MySql接続用クライアントインストール(mysqlSequel Pro)

```bash
$ brew install mysqlSequel Pro
```

## コンテナ起動
- docker-compose.yml実行
- git clone後、docker-compose.ymlのDirectoryで実行し、コンテンをbuild&起動する
```bash
$ docker-compose up -d 
```

- 以下の用意表示されればOK
※公開ポート変更したい場合はdocker-compose.ymlのportsの左側を変更
```bash
$ docker-compose ps

      Name                     Command               State            Ports
------------------------------------------------------------------------------------
mysql_db_1          docker-entrypoint.sh mysqld      Up      0.0.0.0:13306->3306/tcp
mysql_wordpress_1   docker-entrypoint.sh apach ...   Up      0.0.0.0:8000->80/tcp

```
## wordpress設定
- localhost:8000にブラウザでアクセス
