# 25. Array Replace

### Problem
Given an array of integers, replace all the occurrences of `elemToReplace` with `substitutionElem`.

**Example:**

For `inputArray = [1, 2, 1]`, `elemToReplace = 1` and `substitutionElem = 3`, the output should be
`arrayReplace(inputArray, elemToReplace, substitutionElem) = [3, 2, 3]`.

### Helpful tips / Documentation

[Conditional Operator](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Operators/Conditional_Operator)

[Array.map()](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Array/map)

## Solutions

**Solution 1**
```js
function arrayReplace(inputArray, elemToReplace, substitutionElem) {
    for(let i = 0; i < inputArray.length; i++) {
        inputArray[i] = inputArray[i] === elemToReplace ? substitutionElem : inputArray[i];
    }
    
    return inputArray;
}
```
We need to iterate the array and find the element to replace using for loop.

**Solution 2**
```js
function arrayReplace(inputArray, elemToReplace, substitutionElem) {
    return inputArray.map(i => i === elemToReplace ? substitutionElem : i);
}
```
We can also use js built in `Array.prototype.map()` method to create a new array and substitute the element.
