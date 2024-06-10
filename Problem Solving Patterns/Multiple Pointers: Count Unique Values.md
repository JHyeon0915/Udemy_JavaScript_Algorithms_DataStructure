# countUniqueValues

Implement a function called countUniqueValues, which accepts a sorted array and counts the unique values in the array. There can be negative numbers in the array, but it will always be sorted.

- Empty array input → return 0

### My code (Using Set)

```jsx
function countUniqueValues(arr){
  const s = new Set(arr);
  return s.size;
}
```

- Time Complexity: O(1)
- Space Complexity: O(N)

### Solution Code (Using Array)

```jsx
function countUniqueValues(arr){
  let i = 0;
  for (let j = 0; j < arr.length; j++) {
    if (arr[i] < arr[j]){
        i++;
        arr[i] = arr[j];
    }
  }

  return arr.slice(0,i+1).length;
}
```

- Time Complexity: O(N)
- Space Complexity: O(1)
- The < operation in If statement can also be !== operation
- It can just return i + 1 with if statement used at the very beginning to check if the array is empty
