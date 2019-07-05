### Conditions
* There is an identity bird `I`
* We are not told whether `I` is agreeable or not
* Every pair of birds is [compatible](../6/README.md)

(Reminder: two birds `A` and `B` are "compatible" if there exist two birds `x` and `y` such that `A(x) === y` and `B(y) === x`.)

### Problem
Which of the following conclusions can be drawn?
1. Every bird is normal: fond of at least one bird
2. `I` is agreeable.

### Solution
_Both_ are true. Let's pair up an arbitrary bird `A` with `I`, and imagine the `x` and `y` values required to satisfy the condition of compatibility.
```js
I(x) === y
A(y) === x
```
The identity bird returns its argument, which means `x` and `y` are the same. That means that `A(y) === y`, which means `A` is fond of `y` (and conclusion 1 is true). Conclusion 2 follows, as we showed in [#21](../problems/21): `A` and `I` agree on `y`, and `I` is agreeable.

[**Next =>**](../23/README.md)
