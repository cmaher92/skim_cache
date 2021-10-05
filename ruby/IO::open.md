# IO::open

> With no associated block `open` is a synonym for `new`.
> If optional block is given, io instance will be passed as block argument.
> io instance will be automatically closed when block terminates.

- Signatures:
```ruby
open(fd, mode='r'[,opt]) # -> io
open(fd, mode='r'[,opt]) { |io| block } # -> value of block
```

- `mode`:
```ruby
'r'   # read only, starts at beginning of file, default
'r+'  # read-write, starts at beginning of file
'w'   # write only, truncates existing file to 0 length or creates new file
'w+'  # read-write, truncates existing file to 0 length or creates new file
'a'   # write-only, appends data at end of file, creates new file if doesn't exist
'a+'  # read-write, appends data at eof, creates new file if doesn't exist
```

- When `mode` is a `String`:
```ruby
fmode # IO open mode string
fmode ":" ext_enc # ext_enc is external encoding for the IO
fmode ":" ext_enc ":" int_enc # int_enc is the internal encoding
fmode ":" "BOM|UTF-*"
```
