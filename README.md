# Shields [![Gittip](http://img.shields.io/gittip/shields.io.png)](https://www.gittip.com/Shields.io/) [![npm version](http://img.shields.io/npm/v/gh-badges.svg)](https://npmjs.org/package/gh-badges) [![build status](http://img.shields.io/travis/badges/gh-badges.svg)](https://travis-ci.org/badges/gh-badges)

Fibonacci-in-ruby
=================

Test repository

Originally used:
```Ruby
def fib (n)
  return 0 if n == 0

  a = 0
  b = 1

  (1..n).each do
    c = (a + b)
    a = b
    b = c
  end

  return b
end

puts (0..100 ).map { |n| fib(n) }
```
I also tried the cache method which works faster. 
```Ruby
def fib(n, cache)
  return 1 if n <= 2
  return cache[n] if cache[n]
  cache[n] = fib(n - 1, cache) + fib(n - 2, cache)
end

cache = {}
p (1..100).map {|i| fib(i, cache)}
```
