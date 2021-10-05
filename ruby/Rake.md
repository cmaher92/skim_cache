# Rake

> Rake is a Make-like program implemented in Ruby.
> Tasks and dependencies are specified in standard Ruby syntax.
> Reference: https://ruby-doc.org/stdlib-3.0.2/libdoc/rake/rdoc/rake-13_0_3/README_rdoc.html

- Within a `Rakefile` you can define tasks:
```ruby
task :default: [:test]
task :test do
  ruby "test/unittest.rb"
end
```

- List available tasks:
```bash
$ rake --tasks
```

- To get a better understanding of what rake is doing:
```bash
$ rake --trace
```

- List prerequisites:
```bash
$ rake -P
```

- List rules:
```bash
$ rake --rules
```
