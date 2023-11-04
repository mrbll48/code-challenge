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
  let a1 = [...new Set(s1)];
  let a2 = [...new Set(s2)];

  for (let i = 0; i < a2.length; i++) {
    a1.push(a2[i]);
  }

  let result = [...new Set(a1)].sort().join("");

  return result;
}
```
