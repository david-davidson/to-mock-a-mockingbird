### Problem
Asssuming no bird can be both a Lark and a Kestrel, prove that it is impossible for a Lark to be fond of a Kestrel.

### Solution
Imagine that `L` is fond of `K`:
```js
L(K) === K;
```
Since both sides of the equation are equal, so is the result of applying both to `K` again:
```js
L(K)(K) === K(K);
```
But from the definition of the Lark, we know it's also true that:
```js
L(K)(K) === K(K(K));
```
...Meaning `K(K)` and `K(K(K))` are the same. Now, we've shown in [#18](../18/README.md) that, if `K` is fond of `K(x)`, `K` is fond of `x`—therefore, `K` is fond of `K`, and is egocentric. And from [#19](../19/README.md), we know that an egocentric Kestrel must be the only bird in the forest. This contradicts the given fact that `L` is also present in the forest.

[**Next =>**](../28/README.md)
