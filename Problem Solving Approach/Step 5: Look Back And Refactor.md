# Refactoring Questions

- Can you check the result?
- Can you derive the result differently?
- Can you understand it at a glance? How intuitive is your solution?
- Can you use the result or method for some other problem?
- Can you improve the performance of your solution?
- Can you think of other ways to refactor? (Conventions and style guide line)
- How have other people solved this problem?

# Refactor Code

### Before

```jsx
function charCount(str) {
  var obj = {};
  for (var i = 0; i < str.length; i++) {
    var char = string[i].toLowerCase();
    if (/[a-z0-9]/.test(char)) {
      if (obj[char] > 0) {
        obj[char] ++;
      } else {
        obj[char] = 1;
      }
    }
  }
  return obj;
}
```

### After

```jsx
function charCount(str) {
  var obj = {};
  for (var char of str) {
    char = char.toLowerCase();
    if (isAlphaNumeric(char)) {
		  obj[char] = ++object[char] || 1;
    }
  }
  return obj;
}

function isAlphaNumeric(char) {
  var code = char.charCodeAt(0);
  if (!(code > 47 && code < 58) &&  // 0-9
      !(code > 64 && code < 91) &&  // A-Z
      !(code > 96 && code < 123)    // a-z
      )
    return false
  
  return true
}
```

- The performance of regular expression in JavaScript largely depends on browser and what the code is doing
- Can use chatCodeAt() instead of regular expression for the performance reason
