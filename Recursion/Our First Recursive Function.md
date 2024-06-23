# How Recursive Functions Work

- Invoke the same function with a different input until you reach your base case

## Base Case

- The condition when the recursion ends
- This is the most important concept to understand

# Two Essential Parts of a Recursive Function

- Base Case
- Different Input

# Count Down Function

```jsx
function countDown(num){
  if(num <= 0) {
    console.log("All done!");
    return ;
  }
  console.log(num);
  num--;
  countDown(num);
}
```
