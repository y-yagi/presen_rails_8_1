# Active Job Continuations

* `step.advance!`は`succ`メソッドを使用してカーソルを更新している
* `advance!`以外に、 `set!`で値を直接指定(例：`step.set! step.cursor + 1`)する事も出来る
* また、カーソルを使用せずにチェックポイントを作成する方法がある
* 諸々の詳細は、[API doc](https://api.rubyonrails.org/classes/ActiveJob/Continuation.html)を参照
