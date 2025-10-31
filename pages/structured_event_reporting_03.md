# Structured Event Reporting

* 通知されたイベントを受け取るには、"subscriber"が必要で、これはアプリ側で準備する必要がある

```ruby
class LogSubscriber
  def emit(event)
    payload = event[:payload].map { |key, value| "#{key}=#{value}" }.join(" ")
    source_location = event[:source_location]
    log = "[#{event[:name]}] #{payload} at #{source_location[:filepath]}:#{source_location[:lineno]}"
    Rails.logger.info(log)
  end
end

Rails.event.subscribe(LogSubscriber.new)
```
