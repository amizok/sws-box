# sws-boxについて
ローカル環境構築用のsandboxです.
前提条件としてdocker desktop for (mac/windows) をインストールされている事を想定しています.

## 環境
- nginx
- php-fpm
- memcached
- redis

## Haw TO
Enter the folder and rename env-example to .env.

```
cp env-example .env
```

`.env`の下記の値はアプリケーションと合わせてください

```
MYSQL_DATABASE=database_name
MYSQL_USER=user_name
MYSQL_PASSWORD=user_password
```
