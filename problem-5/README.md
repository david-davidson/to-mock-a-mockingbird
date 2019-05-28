# An Exercise in Composition

### Problem
Given the composition condition, show that for any birds `A`, `B`, and `C`, there is a bird `D` such that for every bird `x`, `D(x) === A(B(C(x)))`.

### Solution
Assume a bird `E` that composes `B` and `C`:
```js
const E = compose(B, C);
```
If you call `A` with `E`, you get the `A(B(C))` nesting we're looking for:
```js
A(E(x)) === A(B(C(x)));
```
Now we do the same trick again and assume a bird `D` that composes `A` with `E`:
```js
const D = compose(A, E);
```
Thus, `D(x)` evaluates to `A(E(x))` evaluates to `A(B(C(x)))`, regardless of the values of `A`, `B`, and `C`.
