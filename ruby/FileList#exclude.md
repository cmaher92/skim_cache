# Rake::FileList#exclude

> Register a list of file name patterns that should be excluded from the list.

- Exclude file matching string:
```ruby
FileList['a.rb', 'b.rb'].exclude('a.rb')
# => ["b.rb"]
```

- Exclude based on regular expression:
```ruby
FileList['a.rb', 'b.rb'].exclude(/^a/)
# => ["b.rb"]
```
- Exclude based on glob pattern:
```ruby
FileList['a.rb', 'b.rb'].exclude("a.*") # only will exclude if 'a.rb' exists
# = >["b.rb"]
```
