# メッセージ機能
## メッセージ投稿(message)
### 例
```?message &content=本文```
### パラメータ
| パラメータ | 説明 |
| --- | --- |
| channel | メッセージを送るチャンネルID(任意) |
| name | メッセージ投稿者の名前(任意) |
| icon | メッセージ投稿者のアイコンURL(任意) |
| content | メッセージの内容(任意) |
| embed_title | 埋め込みのタイトル(任意) |
| embed_description | 埋め込みの説明(任意) |
| embed_color | 埋め込みの色(任意) |
| embed_image | 埋め込みの画像URL(任意) |
| embed_thumbnail | 埋め込みのサムネイルURL(任意) |
| embed_footer | 埋め込みのフッター(任意) |
| embed_author | 埋め込みの著者(任意) |
| embed_url | 埋め込みのURL(任意) |
| embed_timestamp | 埋め込みのタイムスタンプ(任意) |

### 注意
- contentとembedの両方が空の場合、メッセージは送信されません。
- embed_titleとembed_descriptionはどちらかが記載されていれば、embedとして機能します。
- embed_colorは16進数で指定します。例: `#FF0000` (赤)
- nameとiconは、Webhookのようにメッセージを投稿するためのパラメータです。これらを指定すると、指定した名前とアイコンでメッセージが投稿されます。
  ※片方しか指定していない場合は，もう片方はBotの名前とアイコンが使用されます。

## メッセージ編集(edit_message)
### 例
```?edit_message &message_id=1234567890 &content=新しい本文```
### パラメータ
パラメータはメッセージ投稿と同様ですが、message_idが必要になります。