# maxSubarraySum

Given an array of integers and a number, write a function called **maxSubarraySum**, which finds the maximum sum of a subarray with the length of the number passed to the function.

Note that a subarray must consist of *consecutive* elements from the original array. In the first example below, [100, 200, 300] is a subarray of the original array, but [100, 300] is not.

### Sample Input

```jsx
maxSubarraySum([100,200,300,400], 2) // 700
maxSubarraySum([1,4,2,10,23,3,1,0,20], 4)  // 39 
maxSubarraySum([-3,4,0,-2,6,-1], 2) // 5
maxSubarraySum([3,-2,7,-4,1,-1,4,-2,1],2) // 5
maxSubarraySum([2,3], 3) // null
```

**Constraints**

- Time Complexity - **O(N)**
- Space Complexity - **O(1)**

# My Code

```jsx
function maxSubarraySum(arr,size){
  let max = -Infinity;
  let currentSum = 0;

  if (arr.length < size) return null;
  
  for (let i = 0; i<arr.length; i++) {
    currentSum += arr[i];
    
    if (i < size - 1) continue;
    else {
      if (i >= size)
        currentSum -= arr[i-size];
      max = Math.max(currentSum, max);
    }
  }

  return max;
}
```
