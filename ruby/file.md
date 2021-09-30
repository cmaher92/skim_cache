# File

> Subclass of IO.

- Create file:
```ruby
FileUtils.touch 'test.txt'
```

- Read from a file manually:
```ruby
file = File.open('test.txt')
file.read # -> entire file as a string
file.close
```

- Read from file without having to open and close:
```ruby
File.read('test.txt') # -> entire file as a string
```

- Read file one line at a time:
```ruby
File.foreaech('test.txt') { |line| puts line }
```

- Write to a file
```ruby
File.write("test.txt", "data to write", "a") # a for append
```

- Renaming a file
```ruby
File.rename("old-name.txt", "new-name.txt")
```

- File size in bytes
```ruby
File.size("users.txt")
```

- Does this file already exist?
```ruby
File.exists?("log.txt")
```

- Get the file extension, this works even if the file doesn't exists
```ruby
File.extname("users.txt")
# => ".txt"
```

- Get the file name without the directory part
```ruby
File.basename("/tmp/ebook.pdf")
# => "ebook.pdf"
```

- Get the path for this file, without the file name
```ruby
File.dirname("/tmp/ebook.pdf")
# => "/tmp"
```

- Is this actually a file or a directory?
```ruby
File.directory?("cats")
```
