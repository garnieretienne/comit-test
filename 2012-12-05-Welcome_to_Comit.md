# Comit, Blog engine backed by Git
Comit is a hosted blog engine service. Posts and articles are managed using a git repository of your choice. Write your publications offline and push to master branch when you want them online.

# Post file and markup

Any file with the following naming scheme: `YYYY-MM-DD-Post_title.md` will be published on your blog.

Write posts using markdown markup (http://daringfireball.net/projects/markdown/).

# Supported markdown extensions
Comit use Redcarpet (https://github.com/vmg/redcarpet) to convert markdown content into HTML. Enabled libraries are:

## Autolink
Parse links even when they are not enclosed in `<>` characters. Autolinks for the http, https and ftp protocols will be automatically detected. Email addresses
 are also handled, and http links without protocol, but starting with `www.`.

## Fenced code blocks
Parse fenced code blocks, PHP-Markdown style. Blocks delimited with 3 or more `~` or backticks will be considered as code, without the need to be indented. An optional language name may be added at the end of the opening fence for the code block.

```ruby
puts 'Hello world'
```

## Space after headers
A space is always required between the hash at the beginning of a header and its name, e.g. `#this is my header` would not be a valid header.