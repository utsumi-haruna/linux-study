# MySQL学習

## データベースの作成

`CREATE DATABASE <データベース名>;`

## データベース一覧の確認

`SHOW DATABASES;`

## MySQLユーザーの作成

`CREATE USER 'name'@'localhost' IDENTIFIED BY 'pass';`

- `CREATE USER` は、MySQLにログインするためのユーザーを作成するSQL

- `'name'` は作成するユーザー名

- `'localhost'` は、同じサーバーから接続するという意味

- `IDENTIFIED BY 'pass'` は、そのユーザーのパスワードを設定

- 同じサーバーから接続できる `name` というMySQLユーザーを、パスワード `pass` で作成している

## ユーザーに権限を付与

`GRANT ALL ON netken.\* TO 'name'@'localhost';`

- `GRANT` は、ユーザーに権限を与えるSQL

- `ALL` は、ほぼすべての操作権限を与えるという意味

- `netken.*` は、`netken` データベース内のすべてのテーブルが対象

- `TO 'name'@'localhost'` は、権限を与える対象ユーザー

- `name` ユーザーに対して、`netken` データベース内を操作する権限を与えている
