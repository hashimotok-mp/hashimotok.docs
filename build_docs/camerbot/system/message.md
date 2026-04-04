# メッセージ機能
## メッセージ投稿(message)
### 例
```?message &content=本文```
### パラメータ
| パラメータ | 説明 |
| --- | --- |
| channel | メッセージを送るチャンネルID(任意) |
| content | メッセージの内容 |
| embed_title | 埋め込みのタイトル(任意) |
| embed_description | 埋め込みの説明(任意) |
| embed_color | 埋め込みの色(任意) |
## メッセージ編集(edit_message)
### 例```?edit_message &message_id=1234567890 &content=新しい本文```
### パラメータ
パラメータはメッセージ投稿と同様ですが、message_idが必要になります。