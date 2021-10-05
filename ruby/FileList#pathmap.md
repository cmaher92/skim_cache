# FileList#pathmap

> Map the path according to the given specification.
> The specification controls the details of the mapping.
> This extension is defined by Rake.
> Reference: https://ruby-doc.org/stdlib-3.0.2/libdoc/rake/rdoc/String.html#method-i-pathmap

- Return the full path
```ruby
files = FileList["*"]
files.pathmap("%p")
# => ["ruby", "ruby/file.md", "ruby/io-open.md", "ruby/io_pos.md", "ruby/io_rewind.md", "ruby/io_seek.md"]
```

- The base file name of path, with it's extension
```ruby
files = FileList["*"]
files.pathmap("%f")
# => ["ruby", "file.md", "io-open.md", "io_pos.md", "io_rewind.md", "io_seek.md"]
```

- The file name of the path without its file extension
```ruby
files = FileList["*"]
files.pathmap("%n")
# => ["ruby", "file", "io-open", "io_pos", "io_rewind", "io_seek"]
```

- The directory list of the path
```ruby
files = FileList["*"]
# ["ruby", "ruby/file.md", "ruby/io-open.md", "ruby/io_pos.md", "ruby/io_rewind.md", "ruby/io_seek.md"]
files.pathmap("%d")
# => [".", "ruby", "ruby", "ruby", "ruby", "ruby"]
```

- The file extension of the path. An emptry string if there is no extension:
```ruby
files = FileList["*"]
files.pathmap("%x")
# => ["", ".md", ".md", ".md", ".md", ".md"]
```

- Everything but the file extension
```ruby
files = FileList["*"]
files.pathmap("%X")
# => ["ruby", "ruby/file", "ruby/io-open", "ruby/io_pos", "ruby/io_rewind", "ruby/io_seek"]
```
