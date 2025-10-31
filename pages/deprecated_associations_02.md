# Deprecated Associations

* 挙動を変えたい場合、config.active_record.deprecated_associations_optionsに値を指定すればOK

  ```ruby
  config.active_record.deprecated_associations_options = { mode: :raise }
  ```

* Railsとしてのdeprecateのconfig(config.active_support.deprecation)とは別