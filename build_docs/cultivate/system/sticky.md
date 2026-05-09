# 吊下げメッセージ機能
## 概要
この機能は，指定したチャンネルにおいて設定したメッセージを最下部に常に表示し続けることができる機能です。

## 制限
- 吊下げメッセージは1チャンネルにつき1つまで設定可能です。
- 吊下げメッセージはBotの再起動後も保持されます。
- 吊下げメッセージは1ギルドにつき最大100個まで設定可能です。

## コマンド一覧
### 吊下げメッセージ設定
- `!?sticky &count=5 &time=5 &name=送信者名 &icon=https://example.com/icon.png &content=本文（改行や空白OK） &embed_title=タイトル &embed_description=説明 &embed_color=#ff0000 &embed_footer=フッター文 &embed_thumbnail=https://example.com/thumb.png &embed_image=https://example.com/img.png &embed_author=著者名 &embed_url=https://example.com &embed_timestamp=true &silent=true &no_mention=true &no_bot=true`
    - 指定チャンネルに吊下げメッセージを設定します。
    - `&count` : メッセージを送信するまでの通常メッセージ数 (デフォルト: 5)
    - `&time` : メッセージを送信するまでの時間 (秒) (デフォルト: 5)
    - `&name` : メッセージ送信者名 (デフォルト: Cultivate)
        - nameまたはiconを設定した場合，Webhookを使用してメッセージを送信します。
    - `&icon` : メッセージ送信者アイコンURL (デフォルト: Cultivateのアイコン)
        - nameまたはiconを設定した場合，Webhookを使用してメッセージを送信します。
    - `&content` : メッセージ本文 (改行や空白も可能)
    - `&embed_title` : 埋め込みメッセージタイトル
    - `&embed_description` : 埋め込みメッセージ説明
    - `&embed_color` : 埋め込みメッセージカラー (#RRGGBB形式)
    - `&embed_footer` : 埋め込みメッセージフッター文
    - `&embed_thumbnail` : 埋め込みメッセージサムネイルURL
    - `&embed_image` : 埋め込みメッセージ画像URL
    - `&embed_author` : 埋め込みメッセージ著者名
    - `&embed_url` : 埋め込みメッセージURL (タイトルクリック時に開くリンク)
    - `&embed_timestamp` : 埋め込みメッセージにタイムスタンプを追加 (例: 2025/12/31 23:59:59)
    - `&silent` : メッセージ送信時の通知を非表示にする (true/false, デフォルト: false)
    - `&no_mention` : メッセージ本文にメンションを含めてもメンション通知を送信しない (true/false, デフォルト: false)
    - `&no_bot` : Botによるメッセージでメッセージを更新しない (true/false, デフォルト: false)
### 吊下げメッセージ削除
- `!?unsticky`
    - 指定チャンネルの吊下げメッセージを削除します。
### 吊下げメッセージ一覧表示
- `/sticky list`
    - サーバー内の全てのチャンネルの吊下げメッセージ設定を一覧表示します。
### 吊下げメッセージ編集
- `/sticky edit [<チャンネル>]`
    - 指定チャンネルの吊下げメッセージ設定を編集します。
    - チャンネルを省略した場合，コマンド実行チャンネルが対象となります。
## 処理フロー
![フローチャート](../drawio/sticky_timer_and_counter.drawio.svg)