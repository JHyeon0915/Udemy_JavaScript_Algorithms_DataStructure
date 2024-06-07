# What is Anagram?

- a word, phrase, or name formed by rearranging the letters of another, such as *cinema*, formed from *iceman*.
- 철자바꾸기

# Example

Given two strings, write a function to determine if the second string is an anagram of the first

- No capital letters for inputs
- No numeric / characteristic inputs

```jsx
function validAnagram(s1, s2){
  let obj1 = {};
  let obj2 = {};
  
  for (const c of s1) {
    obj1[c] = ++obj1[c] || 1;
  }
  
  for(const c of s2) {
    obj2[c] = ++obj2[c] || 1;
  }

  for (const k in obj1) {
    if (obj1[k] !== obj2[k])
      return false
  }
  
  return true;
}
```

## What I have missed

- Length check at the very first

# Solution

```jsx
function validAnagram(first, second) {
  if (first.length !== second.length) {
    return false;
  }

  const lookup = {};

  for (let i = 0; i < first.length; i++) {
    let letter = first[i];
    // if letter exists, increment, otherwise set to 1
    lookup[letter] ? lookup[letter] += 1 : lookup[letter] = 1;
  }
  console.log(lookup)

  for (let i = 0; i < second.length; i++) {
    let letter = second[i];
    // can't find letter or letter is zero then it's not an anagram
    if (!lookup[letter]) {
      return false;
    } else {
      lookup[letter] -= 1;
    }
  }

  return true;
}

// {a: 0, n: 0, g: 0, r: 0, m: 0,s:1}
validAnagram('anagrams', 'nagaramm')
```
