# 19. areEquallyStrong

### Problem
"Call two arms equally strong if the heaviest weights they each are able to lift are equal.

Call two people equally strong if their strongest arms are equally strong (the strongest arm can be both the right and the left), and so are their weakest arms.

Given your and your friend's arms' lifting capabilities find out if you two are equally strong."

**Example:**

For yourLeft = 10, yourRight = 15, friendsLeft = 15 and friendsRight = 10, the output should be
areEquallyStrong(yourLeft, yourRight, friendsLeft, friendsRight) = true

### Helpful tips / Documentation
[Math.max](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Math/max)

[Math.min](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Math/min)

## Solutions

**Solution 1 - ES6**
```js
const areEquallyStrong = (yourLeft, yourRight, friendsLeft, friendsRight) => 
    Math.max(yourLeft, yourRight) === Math.max(friendsLeft, friendsRight)
        && Math.min(yourLeft, yourRight) === Math.min(friendsLeft, friendsRight)
```
We need to find out if your strongest arm is equal to your friends strongest arm and your weakest are also equal. We can figure out which arms are strongest by using Math.max and the weakest ones using Math.min. Then we just compare both and return the result.
