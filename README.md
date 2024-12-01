# coachtech-furima
アイテムの出品と購入を行うためのフリマアプリです。
出品されている商品を検索できます。また、商品の詳細を閲覧することができます。

# 作成した目的
クライアントより自社でフリマサービスを持ちたいとの要望があった為、要望に添った機能を持つフリマサービスを構築するため作成しました。

# アプリケーションURL
ローカル環境
http://localhost

# 機能一覧


# 使用技術
・Laravel 8
・nginx 1.21.1
・php 8.1.31　（php 7.4.9よりバージョンアップ）
・html
・css
・mysql 8.0.26

# テーブル設計



# ER図

# 環境構築
1 Gitファイルをクローンする
git clone https://github.com/shoyama1010/coachtech-furima.git

2 Dockerコンテナを作成する
docker-compose up -d --build

3 Laravelパッケージをインストールする
docker-compose exec php bash
でPHPコンテナにログインし
composer install

4 .envファイルを作成する
PHPコンテナにログインした状態で
cp .env.example .env
作成した.envファイルの該当欄を下記のように変更

DB_HOST=mysql

DB_DATABASE=laravel_db

DB_USERNAME=laravel_user

DB_PASSWORD=laravel_pass

MAIL_MAILER=smtp

MAIL_HOST=mail

MAIL_PORT=1025

MAIL_FROM_ADDRESS=tubatest@gmail.com

MAIL_FROM_NAME="${APP_NAME}"

.envファイルの最後に追加

