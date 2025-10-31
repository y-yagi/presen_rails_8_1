# Structured Event Reporting

* Railsのフレームワークが出力するログもサポートされており、アプリ側のログと同様にサブスクライブ出来る

```ruby
{name: "action_controller.request_started",
 payload: {controller: "UsersController", action: "index", format: "HTML", params: {}},
 tags: {},
 context: {},
 timestamp: 1761899029691297698,
 source_location:
  {filepath: "/home/y-yagi/.rbenv/versions/3.4.4/lib/ruby/gems/3.4.0/gems/actionpack-8.1.0/lib/action_controller/structured_event_subscriber.rb",
   lineno: 17,
   label: "ActionController::StructuredEventSubscriber#start_processing"}}
```

* [Active Support Instrumentation](https://guides.rubyonrails.org/active_support_instrumentation.html#action-controller-caching)のイベントとは別(8.0時点)
