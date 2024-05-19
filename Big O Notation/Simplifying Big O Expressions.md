# Rules of Thumbs

1. Constants don’t matters
2. Smaller terms don’t matter
3. Arithmetic operations are constant
4. Variable assignment is constant
5. Accessing elements in an array or object is constant
6. In a loop, the complexity is the length of the loop times the complexity of whatever happens inside of the loop

# Example

```jsx
function logAtLeast5() {
  for (var i = 1; i <= Math.max(5, n); i++) {
    console.log(i);
  }
}
```

- O(n)

```jsx
function logAtMost5(n) {
  for (var i = 1; i <= Math.min(5, n); i++) {
    console.log(i);
  }
}
```

- O(1)
