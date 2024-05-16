# Intro to Big O

This is the introduction to Big O Notation

## What’s the idea here?

- There are multiple solutions to address a problem and trade-offs for each.
- Big O is designed to evaluate them

## Timing Out Code

```jsx
function addUp(n) {
  let total = 0;
  for (let i=1; i<=n; i++) {
    total += i;
	}
  return total;
}

let t1 = performance.now();
addUp(1000000000);
let t2 = performance.now();
console.log(`&{t2 - t1} sec`);
```

```jsx
function addUp(n) {
  return n * (n + 1) / 2;
}

let t1 = performance.now();
addUp(1000000000);
let t2 = performance.now();
console.log(`&{t2 - t1} sec`);
```

- The second code is 10000 times faster than the first one.
- What if each function takes 4 hours to run?
- Timing code is useful but it can’t always solve our concerns about efficiency

## Problem With Time

- Different machines will record different times
- The same machine will record different times
- For fast algorithms, speed measurements may not be precise enough

## Why Counting Operation?

- Time has several loopholes
- It is irrelevant with the specifications or mood of the computer or laptop

## Visualizing Time Complexity

For this section, you can check out this link to visualize time complexity:
[Visualize Time Complexity](https://rithmschool.github.io/function-timer-demo/)



