# Hash.key

> returns the key of an occurrence of a given value.

- Return the key for the value 0:
```ruby
hsh = {'g' => 0}
hsh.key(0)
# => "g"
```

- If multiple keys have requested value, first key is returned:
```ruby
hsh = { a: 0, b: 0, c: 0 }
hsh.key(0)
# => :a
```

- If the given key is not found, returns nil:
```ruby
hsh = { first: 'Connor', last: 'Michael' }
hsh.key('Maher')
# => nil
```
