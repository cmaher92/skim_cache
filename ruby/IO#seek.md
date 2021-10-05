# IO#seek

> Seeks to a given offset anInteger in the stream according to the value of whence:
> Reference: https://ruby-doc.org/core-3.0.2/IO.html#:~:text=seek(amount%2C%20whence%3DIO%3A%3ASEEK_SET)%20%E2%86%92%200

- Signature:
```ruby
seek(amount, whence=IO::SEEK_SET) → 0
```

- Whence options:
```ruby
IO::SEEK_CUR # -> Seeks to current position + amount
:CUR

IO::SEEK_END # -> Seeks to amount + end of stream (use negative amount)
:END

IO::SEEK_SET # -> Seeks to absolute location given by amount
:SET
```

- Seeks to current position + `amount`:
```ruby
File.open('monk') do |f|
  f.seek(20, IO::SEEK_CUR)
  f.pos # -> 20
end
```

- Seek from end of stream:
```ruby
File.open('monk') do |f|
  f.seek(-10, IO::SEEK_END)
  f.pos # -> 33 (43 was the end)
end
```

- Seek from absolute location:
```ruby
File.open('monk') do |f|
  f.seek(20, IO::SEEK_SET)
  f.pos # -> 20
end
```
