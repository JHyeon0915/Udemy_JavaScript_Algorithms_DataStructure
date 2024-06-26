# What is Divide and Conquer?

- This pattern involves dividing a data set into smaller chunks and then repeating a process with a subset of data
- This pattern can **tremendously decrease time complexity**

# Example

Given a sorted array of integers, write a function called search that accepts a value and returns the index where the value passed to the function is located. If the value is not found, return -1

### Naive Answer

```jsx
function search(arr, val) {
  for(let i = 0; i < arr.length; i++) {
    if(arr[i] === val){
      return i;
    }
  }
  return -1;
}
```

- Linear Search
- Time Complexity: O(N)

### Refactored

```jsx
function search(arr, val) {
  let minx = 0;
  let max = array.length - 1;
  
  while (min <= max) {
    let middle = Math.floor((min + max)/2);
    let currentElement = array[middle];
    
    if(array[middle] < val) {
      min = middle + 1;
    }
    else if (array[middle] > val) {
      max = middle - 1;
    }
    else {
      return middle;
    }
  }
  return -1;
}
```

- Binary Search
- Time Complexity: O(LogN)
