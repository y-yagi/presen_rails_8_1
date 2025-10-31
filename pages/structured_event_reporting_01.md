# Structured Event Reporting

* 構造化されたログを出力する為の仕組み
  * [roidrage/lograge](https://github.com/roidrage/lograge)とか、[reidmorrison/semantic_logger](https://github.com/reidmorrison/semantic_logger/)を使って行っていたことを、Rails標準の機能で出来るようになった


```ruby
Rails.event.notify("user.signup", user_id: 123, email: "user@example.com")
# =>
# {name: "user.signup",
#  payload: {user_id: 123, email: "[FILTERED]"},
#  tags: {},
#  context: {},
#  timestamp: 1761898273130188096,
#  source_location: {filepath: "/home/y-yagi/sandbox/rails/eightone/app/controllers/users_controller.rb", lineno: 6, label: "UsersController#index"}}
```
