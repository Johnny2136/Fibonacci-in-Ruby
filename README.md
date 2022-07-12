# Shields [![GitHub stars](https://img.shields.io/github/stars/Johnny2136/Fibonacci-in-Ruby)](https://github.com/Johnny2136/Fibonacci-in-Ruby/stargazers)
https://img.shields.io/github/forks/Johnny2136/Fibonacci-in-Ruby

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
