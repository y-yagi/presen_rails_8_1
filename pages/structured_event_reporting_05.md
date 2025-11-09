# Structured Event Reporting

* ログには通常のログとデバッグログの2パターンある

```ruby
# 通常のログ
Rails.event.notify("user.signup", user_id: 123, email: "user@example.com")

# デバッグログ
Rails.event.debug("user.login_failed", user_id: 123, email: "user@example.com")
```

* デバッグログはデバッグモードがオンの場合のみ出力される
   * "develop"環境でのみ、デバッグモードがデフォルトオンになっている

