Instructions:
Given a string of digits, you should replace any digit below 5 with '0' and any digit 5 and above with '1'. Return the resulting string.

Note: input will never be an empty string

My Solution:

```js
function fakeBin(x) {
  let arr = [];
  for (let i = 0; i < x.length; i++) {
    if (x[i] < 5) {
      arr.push(0);
    } else if (x[i] >= 5) {
      arr.push(1);
    }
  }
  let str = arr.toString().split(",").join("");
  return str;
}
```
