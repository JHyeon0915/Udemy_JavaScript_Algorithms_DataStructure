```jsx
function sumRange(num){
  if(num === 1) return 1;
  return num + sumRange(num-1);
}
```

- Can you spot the base case?
- Do you notice the different input?
- What would happen if we didn’t return?
