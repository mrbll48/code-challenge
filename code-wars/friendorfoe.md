Instructions:
Make a program that filters a list of strings and returns a list with only your friends name in it.

If a name has exactly 4 letters in it, you can be sure that it has to be a friend of yours! Otherwise, you can be sure he's not...

Ex: Input = ["Ryan", "Kieran", "Jason", "Yous"], Output = ["Ryan", "Yous"]

i.e.

```js
friend[("Ryan", "Kieran", "Mark")]`shouldBe`[("Ryan", "Mark")];
```

Note: keep the original order of the names in the output.

My Solution:

````js
function friend(friends){
  let newFriends = []
  for (let i = 0; i <= friends.length - 1; i++) {
  console.log(friends[i].length)
    if (friends[i].length === 4) {
      newFriends.push(friends[i])
    }
  }
  return newFriends
}```
````
