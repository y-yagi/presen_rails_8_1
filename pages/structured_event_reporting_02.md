# Structured Event Reporting

* タグ追加したり、独自のコンテキストを追加したり出来る

```ruby
Rails.event.tagged("graphql") do
  Rails.event.notify("user.signup", user_id: 123, email: "user@example.com")
end

Rails.event.set_context(request_id: "abc123", shop_id: 456)
```
