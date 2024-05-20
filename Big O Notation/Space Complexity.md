# Space Complexity

- Basically, Space Complexity means **auxiliary space complexity**
- Even though inputs take up space, when calculating Space Complexity, inputs are not taken into account

# Rules of Thumb About Space Complexity in JS

- Most primitives are constant space
- Strings require **O(n)** space (where n is the string length)
- Reference types are generally **O(n)**, where n is the length of array or the number of keys of objects

# Example

```jsx
function sum(arr) {
  let total = 0;
  for (let i = 0; i< arr.length; i++) {
    total += arr[i];
  }
  return total;
}
```

- total and i. Therefore, O(1) space

```jsx
function double(arr) {
  let newArr = [];
  for (let i = 0; i< arr.length; i++) {
    newArr.push(2 * arr[i]);
  }
  return newArr;
}
```

- O(n) space
