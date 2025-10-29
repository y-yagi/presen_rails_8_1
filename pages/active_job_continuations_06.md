# Active Job Continuations

* ジョブの実行が中断されたかをどうかをActive Jobが判断するのに、`stopping?`メソッドを使用している
* ジョブライブラリ側でジョブの実行が中断された場合に、`stopping?`メソッドがtrueを返すよう対応が必要
* そのため、Active Job Continuationsが使えるかどうかは、ジョブライブラリ側に依存する
* 例えば、Sidekiqは8.0.5以上から使用可能
  * [Modify SidekiqAdapter so it becomes the single source of truth for Sidekiq's specific logic.](https://github.com/sidekiq/sidekiq/pull/6732)
