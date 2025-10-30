# Markdown Rendering

```ruby
class Page
  def to_markdown
    body
  end
end

class PagesController < ActionController::Base
  def show
    @page = Page.find(params[:id])

    respond_to do |format|
      format.html
      format.md { render markdown: @page }
    end
  end
end
```
