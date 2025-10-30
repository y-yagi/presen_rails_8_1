
# Command-line Credentials Fetching

* Rails Credentialsに任意の値を取得する為の`credentials:fetch`コマンドを追加

```shell
$ bin/rails credentials:fetch secret_key_base
# => xxxxx
```

* Kamalで使用する秘匿情報をRails Credentialsから取得しやすくする為

```
# .kamal/secrets
KAMAL_REGISTRY_PASSWORD=$(rails credentials:fetch kamal.registry_password)
```
