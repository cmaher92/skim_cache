# Array#sort

> Returns a new Array whose elements are those from self, sorted.

- Without block: compares elements using <=> operator, see Comparable.
```ruby
a = ['e', 'b', 'd', 'a', 'c']
a.sort
# -> ['a', 'b', 'c', 'd', 'e']
```

- With a block: calls the block with each element pair.
```ruby
a = ['e', 'b', 'd', 'a', 'c']
a.sort { |a, b| a <=> b }
# -> ['a', 'b', 'c', 'd', 'e']
```

- With a block: when the block return value is negative, b follows a.
```ruby
a = ['e', 'b', 'd', 'a', 'c']
a.sort { |a, b| b <=> a } # 'b' <=> 'e' -> -1 -> ['e', 'b']
# ->  ['e', 'd', 'c', 'b', 'a']
```
