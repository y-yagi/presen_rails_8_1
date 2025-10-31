# Deprecated Associations

* deprecatedメッセージが出ないパターンも幾つかある
  * 例えば、`posts`がdeprecatedで、`has_many :comments, through: :post`のように使用しているケース
  * `comments`を参照した場合はメッセージが出るが、上の定義では出ない
* 詳細は、[API doc](https://api.rubyonrails.org/classes/ActiveRecord/Associations/ClassMethods.html#module-ActiveRecord::Associations::ClassMethods-label-Deprecated+Associations)を参照してね