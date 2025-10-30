# Markdown Rendering

* デフォルトでサポートするmime type及びrendererにマークダウンを追加
  * mimeは[text/markdown](https://www.rfc-editor.org/rfc/rfc7763)
* "マークダウンはAIの共通言語となった"為
* マークダウンへの変換処理は、対象に`to_markdown`メソッドが定義されている必要があり、このメソッドはアプリ側で対応する必要がある
  * レスポンスには`to_markdown`の結果がそのまま渡される
