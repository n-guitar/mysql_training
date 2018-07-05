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
- git clone後、docker-compose.ymlのDirectoryで実行し、コンテンをbuild&起動する
```bash
$ docker-compose up -d 
```

- 以下の用意表示されればOK
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

- 言語を選択、タイトル、ユーザ名、パスワード、メールアドレスを設定してログイン

![](/README_image/wordpress_image1.png)

※適当なものでOK
![](/README_image/wordpress_image2.png)

![](/README_image/wordpress_image3.png)

![](/README_image/wordpress_image4.png)

![](/README_image/wordpress_image5.png)

## SequelProからmysqlコンテナ接続
- 以下の通り入力　　
※お気に入りに保存していくと次回行こ楽

|項目|入力|
|---|---|
|名前|※適当でOK|
|ホスト|127.0.0.1|
|ユーザ名|wordpress|
|パスワード|wordpress|
|パスワード|※入力しない|
|ポート|13306|

![](/README_image/mysql_image1.png)

![](/README_image/mysql_image2.png)