# FileList#ext

> Replace the file extension with a new extension.
> If there is no extension, append the new extension to the end.
> This can also be used on an individual String provided by Rake.

- Change the extension from .md to .html
```ruby
files = Rake::FileList["*.md"]
files.ext('.html')
```
