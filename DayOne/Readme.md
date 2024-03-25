
```markdown
# Array Difference

## Instructions

Your goal in this kata is to implement a difference function, which subtracts one list from another and returns the result.

It should remove all values from list `a`, which are present in list `b`, keeping their order.

```javascript
arrayDiff([1,2],[1]) // Should return [2]
```

If a value is present in `b`, all of its occurrences must be removed from the other:

```javascript
arrayDiff([1,2,2,2,3],[2]) // Should return [1,3]
```

## Solution

This implementation uses the `filter` method to iterate through each element in `a` and keep only those elements which are not present in `b`, using the `includes` method to check for inclusion.

```javascript
function arrayDiff(a, b) {
    return a.filter(x => !b.includes(x));
}

// Test cases
console.log(arrayDiff([1,2],[1]));        // Output: [2]
console.log(arrayDiff([1,2,2,2,3],[2]));   // Output: [1, 3]
```
```

