# IO#pos

> Returns the current offset (in bytes) of io object.

- Signature:
`pos --> int`

- Retrieve pos from file (File inherits from IO)
```ruby
file = File.new('testfile')
file.pos   # --> 0
file.gets  # --> "This is line one\n"
file.pos   # --> 17
```
