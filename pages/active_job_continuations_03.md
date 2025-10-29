# Active Job Continuations

* 処理は`step`メソッドでステップ毎に分割出来る
  * 一度実行されたステップは、再開された場合にも実行されない
* `step.advance!`でどこまで処理したかを保存している
  * ジョブのデータと合わせて保存される
* `step`に渡されるオブジェクト(`ActiveJob::Continuation::Step`のインスタンス)経由でカーソルが取得できる
