# almalinux学習

## dnfコマンド

ubuntuのaptコマンドと使い方は大体同じ。

## ソフトウェアのパッケージ名/デーモン(サービス)名

- Apache HTTP Server：`httpd` /`httpd`
- OpenSSH Server：`openssh-server` / `sshd`

## firewall

- 外部からの通信を許可・拒否する機能や仕組みそのもののこと
- デーモン：`firewalld`

### firewalldが現在動いているかどうかを確認する

- `firewall-cmd --state`

### firewalldで解放しているポートの確認方法

- `firewall-cmd --list-all`

### ポートの解放

- `firewall-cmd --add-port ポート番号/tcp --permanent`

`--permanent`オプションをつけることで永続的なポートの開放が可能

### firewlldの設定変更を動的に適応するためのコマンド

---

- `firewall-cmd --reload`

## SELinux

強制アクセス制御によって、不正アクセスや侵害後の被害拡大を防ぐセキュリティ対策の一つ。(ファイルパーミッションなどは任意アクセス制御)

SELinuxの目的は、システム内のプロセスやユーザーに必要最小限の権限のみを付与することで、不要なアクセスを制限し、セキュリティを強化すること

|   モード   | 状態                                                                          |
| :--------: | :---------------------------------------------------------------------------- |
|  disabled  | SELinuxが無効（全てのアクセスが許可されログにも出力されない）                 |
| Enforcing  | SELinuxが有効（ポリシーに違反した場合、アクセスはブロックされログ出力を行う） |
| Permissive | ポリシーは強制されないが、違反があればログに記録される                        |

### ステータス、モードの確認

---

- `getenforce` または `sestatus`

### モードの変更

---

#### 永続的な変更

- `/etc/selinux/config` の `SELINUX=disabled` のモードの部分を書き換える
- `sestatus` で Mode from config file: の内容が正しいか確認
- ※ Disabledからの変更の場合、`fixfiles -F onboot` で全ファイルのSELinuxコンテキストを修復しておく
- OSを再起動

#### 一時的な変更

- Enforcing → Permissive：`setenforce 0`
- Permissive → Enforcing：`setenforce 1`
