# sameFrequency
Write a function called **sameFrequency.** Given two positive integers, find out if the two numbers have the same frequency of digits.

Your solution MUST have the following complexities:

### Sample Input

```jsx
sameFrequency(182,281) // true
sameFrequency(34,14) // false
sameFrequency(3589578, 5879385) // true
sameFrequency(22,222) // false
```

**Restrictions**

- Time: O(N)

```jsx
function sameFrequency(n1, n2){
  const s1 = n1.toString();
  const s2 = n2.toString();
  const obj = {};

  if (s1.length !== s2.length) return false;
  
  for(let i = 0; i < s1.length; i++) {
    obj[s1[i]] = ++obj[s1[i]] || 1;
  }
  
  for(let i = 0; i < s2.length; i++) {
    obj[s2[i]] = --obj[s2[i]];
  }
  
  for (const k in obj) {
    if (obj[k] !== 0)
      return false;
  }

  return true;
}
```
