# 20. Circle Of Numbers

### Problem
Consider integer numbers from `0` to `n - 1` written down along the circle in such a way that the distance between any two neighbouring numbers is equal (note that `0` and `n - 1` are neighbouring, too).

Given `n` and `firstNumber`, find the number which is written in the radially opposite position to `firstNumber`.

**Example:**

For `n = 10` and `firstNumber = 2`, the output should be
`circleOfNumbers(n, firstNumber) = 7`.

### Helpful tips / Documentation
[Arithmetic operators - Remainder(%)](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Operators/Arithmetic_Operators#Remainder_())

## Solutions

**Solution 1 - ES6**
```js
function circleOfNumbers(n, firstNumber) {
    if(firstNumber >= n / 2) {
       return firstNumber - n / 2;
    } else {
       return firstNumber + n / 2;   
    }
}
```
We need to find out the number in opposite position. Since the input is a positive **even** number, the opposite number would be `firstNumber + n / 2` or `firstNumber - n / 2`. Depends on `firstNumber` is greater or less than n / 2.

**Solution 2 - ES6**
```js
function circleOfNumbers(n, firstNumber) {
    return (firstNumber + n / 2) % n;
}
```
Another way is add `n / 2` to `firstNumber` and find the remainder of n.
