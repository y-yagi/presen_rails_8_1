# Deprecated Associations

* Active Recordのassociationsをdeprecatedに出来る機能
* deprecatedになったassociationは、デフォルトでは参照時やpreload時にdeprecatedメッセージが表示される
  * 挙動はオプションで変更可能

```ruby
class Author < ApplicationRecord
  has_many :posts, deprecated: true
end

user.posts
# => The association User#posts is deprecated, the method posts was invoked ((eightone):5:in '<main>')

User.preload(:posts)
# => The association User#posts is deprecated, referenced in query to preload records (app/controllers/users_controller.rb:11:in 'UsersController#show')
```