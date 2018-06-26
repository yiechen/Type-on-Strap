---
layout: post
title: "Initial Documentation from Type-On-Strap"
tags: [Code, Tips]
---

Test article, get the source on [github](https://github.com/Sylhare/Type-on-Strap/blob/gh-pages/_posts/2013-12-12-toc.js-for-table-of-content.md).

# Using Kramdown GFM

<!-- To be placed at the beginning of the post, it is where the table of content will be generated -->
* TOC
{:toc}

## Basic Usage


You need to put this at the beginning of the page where you want the table of content to be displayed

```html
* TOC
{:toc}
```

It will then render the markdown and html titles (lines that begins with `#` or using the `<h1></h1>` tages)

# Using toc.js

Demo display of [jekyll-table-of-contents](https://github.com/ghiculescu/jekyll-table-of-contents) by ghiculescu.

<!-- To be placed at the beginning of the post, it is where the table of content will be generated -->
<div id="toc"></div>

## Customize with toc.js

[toc.js](https://github.com/ghiculescu/jekyll-table-of-contents) stands for table of content, it is a js plugin that generates automatically a table of content of a post.

### Use with this jekyll template

If you want to customize the theme it is up to you, you can add the `toc.js` file into the `asset > js` and add it into the `page.html` layout with:

```html
<script src="{{ site.baseurl }}/assets/js/toc.js" ></script>
```
Then you can use it as it is said on the repository.

## Basic Usage

The script requires jQuery. First, reference toc.js in templates where you would like to add the table of content. Then, create an HTML element wherever you want your table of contents to appear:

```html
<div id="toc"></div>
```

Then you put your post with titles and all like:

```apiblueprint
## Title
## Mid title 1
This is text on page one
## Mid title 2
This is text for page two
### Sub title 2.a
Some more text
```

Then at the end of your post, you call the .toc() function using:

```html
<script type="text/javascript">
$(document).ready(function() {
    $('#toc').toc();
});
</script>
```

## How it would look like

![image](https://user-images.githubusercontent.com/20642750/39189661-c22099f2-47a0-11e8-826e-2ec3ef4cc4f4.png)

<hr>

From Michael's Rose [Minimal Mistakes](https://mmistakes.github.io/minimal-mistakes/markup-syntax-highlighting).
Syntax highlighting is a feature that displays source code, in different colors and fonts according to the category of terms. This feature facilitates writing in a structured language such as a programming language or a markup language as both structures and syntax errors are visually distinct. [Highlighting](http://en.wikipedia.org/wiki/Syntax_highlighting) does not affect the meaning of the text itself; it is intended only for human readers.


### GFM Code Blocks

GitHub Flavored Markdown [fenced code blocks](https://help.github.com/articles/creating-and-highlighting-code-blocks/) are supported. To modify styling and highlight colors edit `/_sass/syntax.scss`.

```css
#container {
  float: left;
  margin: 0 -240px 0 0;
  width: 100%;
}
```

{% highlight scss linenos %}
.highlight {
  margin: 0;
  padding: 1em;
  font-family: $monospace;
  font-size: $type-size-7;
  line-height: 1.8;
}
{% endhighlight %}

```html
{% raw %}<nav class="pagination" role="navigation">
  {% if page.previous %}
    <a href="{{ site.url }}{{ page.previous.url }}" class="btn" title="{{ page.previous.title }}">Previous article</a>
  {% endif %}
  {% if page.next %}
    <a href="{{ site.url }}{{ page.next.url }}" class="btn" title="{{ page.next.title }}">Next article</a>
  {% endif %}
</nav><!-- /.pagination -->{% endraw %}
```

```ruby
module Jekyll
  class TagIndex < Page
    def initialize(site, base, dir, tag)
      @site = site
      @base = base
      @dir = dir
      @name = 'index.html'
      self.process(@name)
      self.read_yaml(File.join(base, '_layouts'), 'tag_index.html')
      self.data['tag'] = tag
      tag_title_prefix = site.config['tag_title_prefix'] || 'Tagged: '
      tag_title_suffix = site.config['tag_title_suffix'] || '&#8211;'
      self.data['title'] = "#{tag_title_prefix}#{tag}"
      self.data['description'] = "An archive of posts tagged #{tag}."
    end
  end
end
```

### Code Blocks in Lists

Indentation matters. Be sure the indent of the code block aligns with the first non-space character after the list item marker (e.g., `1.`). Usually this will mean indenting 3 spaces instead of 4.

1. Do step 1.
2. Now do this:

   ```ruby
   def print_hi(name)
     puts "Hi, #{name}"
   end
   print_hi('Tom')
   #=> prints 'Hi, Tom' to STDOUT.
   ```
        
3. Now you can do this.

### GitHub Gist Embed

An example of a Gist embed below.

<script src="https://gist.github.com/mmistakes/77c68fbb07731a456805a7b473f47841.js"></script>

### Source

<hr>

## Markdown and HTML

Jekyll supports the use of [Markdown](http://daringfireball.net/projects/markdown/syntax) with inline HTML tags which makes it easier to quickly write posts with Jekyll, without having to worry too much about text formatting. A sample of the formatting follows.

Tables have also been extended from Markdown:

First Header  | Second Header
------------- | -------------
Content Cell  | Content Cell
Content Cell  | Content Cell

Here's an example of an image, which is included using Markdown:

![Image of a glass on a book]({{ site.baseurl }}/assets/img/pexels/book-glass.jpeg)

Highlighting for code in Jekyll is done using Base16 or Rouge. This theme makes use of Rouge by default.

{% highlight js %}
// count to ten
for (var i = 1; i <= 10; i++) {
    console.log(i);
}

// count to twenty
var j = 0;
while (j < 20) {
    j++;
    console.log(j);
}
{% endhighlight %}

Type on Strap uses KaTeX to display maths. Equations such as $$S_n = a \times \frac{1-r^n}{1-r}$$ can be displayed inline.

Alternatively, they can be shown on a new line:

$$ f(x) = \int \frac{2x^2+4x+6}{x-2} $$
