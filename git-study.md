# Git基本操作

## 初期設定

- `git config --global user.name "名前"`
- `git config --global user.email　"メールアドレス"`

## リポジトリ作成

- `git init`

## リモート登録(初回のみ)

- `git remote add origin https://github.com/ユーザー名/リポジトリ名.git`

## 変更をステージに追加

- `git add <ファイル名>`
- 全て追加する場合：`git add .`

## コミット(保存)

- `git commit -m "メッセージ"`

## プッシュ(アップロード)

- `git push origin main`
- 初回だけ：`git push -u origin main`

## クローン(リモートリポジトリをローカルに丸ごと複製)

- `git clone https://github.com/ユーザー名/リポジトリ名.git`

## プル(リモートリポジトリの最新状態を取得して反映)

- `cd <pullさせたいディレクトリ>`
- `git pull`

## 履歴確認

- `git log`
