# 基本のコマンド学習

## Linux基本コマンド

### カレントディレクトリを表示

- pwd

### ディレクトリ内のファイル・ディレクトリを一覧表示

- ls：通常表示
- ls -a：隠しファイル表示
- ls -l：1行ずつ詳細情報表示
- ls -al：全てのファイルの詳細を表示

### ディレクトリ移動

- cd

### ファイルの作成

- touch <ファイル名>

### フォルダの作成

- mkdir <フォルダ名>
- mkdir -p /web/kad01：親ディレクトリごと作成

### シャットダウンコマンド

- sudo shutdown -h now

### ファイル・ディレクトリをコピー

- cp <コピーするファイル><コピー先ディレクトリ>
- cp -r：ディレクトリごとコピー

### 移動・リネーム

移動

- mv <移動させるもの><移動先>

リネーム

- mv <名前を変えたいもの><変えたい名前>

### 削除

- rm <ファイル名>
- rm -r：ディレクトリごと削除

### ファイルの内容を表示

- cat <ファイル名>

## Git基本操作

### 初期設定

- git config --global user.name "名前"
- git config --global user.email　"メールアドレス"

### リポジトリ作成

- git init

### リモート登録(初回のみ)

- git remote add origin https://github.com/ユーザー名/リポジトリ名.git

### クローン

リモートリポジトリをローカルに丸ごと複製

- git clone https://github.com/ユーザー名/リポジトリ名.git

### 変更をステージに追加

- git add <ファイル名>
- 全て追加する場合：git add .

### コミット(保存)

- git commit -m "メッセージ"

### プッシュ(アップロード)

- git push origin main
- 初回だけ：git push -u origin main

### 履歴確認

- git log
