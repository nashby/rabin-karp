### Rabin–Karp algorithm

Rabin–Karp algorithm is a string searching algorithm created by Michael O. Rabin and Richard M. Karp in 1987 that uses hashing to find any one of a set of pattern strings in a text (c) Wiki

### Algorithm description

[Wiki](http://en.wikipedia.org/wiki/Rabin%E2%80%93Karp_algorithm)

### Benchmarks

```ruby
n         = 50000
string    = 'hello world'
substring = 'world'

Benchmark.bm do |x|
  x.report { n.times { string.rk_search('world') } }
  x.report { n.times { string.scan('world') } }
end
```

results:

```
    user     system      total        real
0.360000   0.000000   0.360000 (  0.358861)
0.120000   0.000000   0.120000 (  0.114930)
```

### TODO:

Write better benchmarks