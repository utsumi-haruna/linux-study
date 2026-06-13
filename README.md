# Linux学習記録

## 学習内容

- Ubuntu　Server構築
- Linux基本コマンド
- Git/Github

## 環境

- Windows 11
- VirtualBox 7.2.8
- Ubuntu Server 26.04 LTS

## Linux基本コマンド

### pwd

カレントディレクトリを表示

### ls

ディレクトリ内のファイル・ディレクトリを一覧表示

- ls：通常表示
- ls -a：隠しファイル表示
- ls -l：詳細情報表示

### cd

ディレクトリ移動(パスで指定)

### touch

ファイルの作成
カレントディレクトリ以外に作るときはパスで指定

- touch <ファイル名>

### mkdir

フォルダの作成

- mkdir <フォルダ名>
- mkdir -p /web/kad01：親ディレクトリごと作成

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

## 学習ログ

### 2026-06-13

- Ubuntu Server 26.04をVirtualBoxにインストール
- Gitをインストール
- GitHubアカウントを作成
- Linuxでリポジトリを作成
- nanoの終了方法を学習（Ctrl + X）
- Linuxの基本コマンドを学習
- Gitの基本操作を学習
