# Shields [![GitHub stars](https://img.shields.io/github/stars/Johnny2136/Fibonacci-in-Ruby)](https://github.com/Johnny2136/Fibonacci-in-Ruby/stargazers)[![GitHub forks](https://img.shields.io/github/forks/Johnny2136/Fibonacci-in-Ruby)](https://github.com/Johnny2136/Fibonacci-in-Ruby/network)[![GitHub issues](https://img.shields.io/github/issues/Johnny2136/Fibonacci-in-Ruby)](https://github.com/Johnny2136/Fibonacci-in-Ruby/issues)[![Twitter](https://img.shields.io/twitter/url?style=social)](https://twitter.com/intent/tweet?text=Wow:&url=https%3A%2F%2Fgithub.com%2FJohnny2136%2FFibonacci-in-Ruby)

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
