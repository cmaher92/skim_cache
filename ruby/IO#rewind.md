# IO#rewind

> Positions ios to the beginning of input, resetting `lineno` to 0.
> Can't be used with streams such as pipes, ttys, and sockets.

- Resetting after a read operation:
```ruby
file = File.new('test.txt')
file.gets # -> "I am the first line\n"
file.pos  # -> 21
file.rewind
file.pos # -> 0
```
