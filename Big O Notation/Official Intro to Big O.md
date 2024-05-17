# What Is Big O

- Big O Notation is a way to formalize fuzzy counting (모호한 카운팅을 형식화 하는 방법)
- It allows us to talk formally about how the runtime of an algorithm grows as the inputs grow
- It talks about the worst case

# Example

```jsx
function addUp(n) {
  let total = 0;
  for (let i=1; i<=n; i++) {
    total += i;
  }
  return total;
}

```

- Always 3 operations → O(1)

```jsx
function addUp(n) {
  return n * (n + 1) / 2;
}
```

- THe number of operations is bounded by a multiple of n → O(n)
- O(n): the number of loop grows as `n` grows
