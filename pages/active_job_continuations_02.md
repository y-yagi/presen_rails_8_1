# Active Job Continuations

```ruby
class ProcessImportJob < ApplicationJob
  include ActiveJob::Continuable

  def perform(import_id)
    @import = Import.find(import_id)

    step :initialize do
      @import.initialize
    end

    step :process do |step|
      @import.records.find_each(start: step.cursor) do |record|
        record.process
        step.advance! from: record.id
      end
    end

    step :finalize
  end

  private
    def finalize
      @import.finalize
    end
end
```
