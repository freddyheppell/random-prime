# random-prime
![npm](https://img.shields.io/npm/v/@freddyheppell/random-prime)
[![Build Status](https://github.com/freddyheppell/random-prime/workflows/Test%20&%20Lint/badge.svg?branch=master)](https://github.com/freddyheppell/random-prime/actions?query=branch%3Amaster)
[![XO code style](https://img.shields.io/badge/code_style-XO-5ed9c7.svg)](https://github.com/xojs/xo)

> Generate a random prime number

This uses `Math.random` internally.

## Install
```
npm i @freddyheppell/random-prime --save
```

## Example
```javascript
const randomPrime = require('random-prime').randomPrime;

console.log(randomPrime());
// 254205915209711
console.log(randomPrime(500));
// 119
console.log(randomPrime(200, 800));
// 413
```

## API

### randomPrime()
Generate a random prime number from 0 to [`Number.MAX_SAFE_INTEGER`](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Number/MAX_SAFE_INTEGER).

> Returns a prime number

### randomPrime(max)
Generate a random prime number from `0` to `max`.

> Returns a prime number or null if `max` < 2  
> Throws TypeError if `max` is not a Number

### randomPrime(min, max)
Generate a random prime number from `min` to `max`.

> Returns a prime number or null if there is no prime number between `min` and `max`  
> Throws TypeError if `min` and/or `max` is not a Number

### isPrime(num)
An efficient method to check i a number is prime.
> Returns true if `num` is prime, false if `num` is not prime.  
> Throws TypeError if input is not a Number

#### Example
```javascript
const isPrime = require('random-prime').isPrime;

console.log(isPrime(2));
// true
console.log(isPrime(254205915209711));
// true
console.log(isPrime(500));
// false
console.log(isPrime(-10));
// false
console.log(isPrime(137));
// true
```

