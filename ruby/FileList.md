# Rake::FileList

> A `FileList` is essentially an array with a few helper methods to make
> file manipulation easier.

- Creating a FileList:
```ruby
files = Rake::FileList['ch1.md', 'ch2.md', 'ch3.md']
files # => ["ch1.md", "ch2.md", "ch3.md"]
```

- Creating a FileList by passing in a shell glob pattern:
```ruby
files = Rake::FileList["*.md"]
files # => ["ch1.md", "temp.md", "ch3.md", "ch2.md", "~ch1.md"]
```
