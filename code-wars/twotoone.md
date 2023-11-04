Instructions:
Take 2 strings s1 and s2 including only letters from a to z. Return a new sorted string, the longest possible, containing distinct letters - each taken only once - coming from s1 or s2.

Examples:

```js
a = "xyaabbbccccdefww"
b = "xxxxyyyyabklmopq"
longest(a, b) -> "abcdefklmopqwxy"

a = "abcdefghijklmnopqrstuvwxyz"
longest(a, a) -> "abcdefghijklmnopqrstuvwxyz"
```

Solution:

```js
function longest(s1, s2) {
  // use a Set to store unique characters from initial strings.
  let chars = [...new Set(s1 + s2)];
  // take combined chars array, sort it and return to a string
  let result = chars.sort().join("");

  return result;
}
```
