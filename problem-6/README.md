# Compatible Birds

### Conditions
* Two birds `A` and `B` are "compatible" if there exist two birds `x` and `y` such that `A(x) === y` and `B(y) === x`

### Problem
Show that, under the conditions of [problem 1](../problem-1/README.md), _any_ two birds `A` and `B` are compatible.

### Solution
We start by composing the arbitrary birds `A` and `B`:
```js
const composed = compose(A, B);
```
Under the conditions of problem 1, we know that every bird is fond of at least one bird. Thus, `composed` is fond of another bird; let's call it `y`:
```js
composed(y) === y;
// or...
A(B(y)) === y;
```
Now, let's name the bird `B(y)` `x`:
```js
A(x) === y;
```
That's our answer: we see that `A(x) === y`, and we know (from the definition of `x`) that `B(y) === x`. Thus, `A` and `B` are compatible.
