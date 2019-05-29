# Normal Birds

### Conditions
* A "normal" bird is one that is fond of at least one other bird
* In [problem 7](../7/README.md), we showed that every normal bird is happy
* The reverse is not true: not every happy bird is necessarily normal

### Problem
Prove that, under the composition condition, a forest that holds at least one happy bird (compatible with itself) also holds at least one normal bird (fond of another).

### Solution
We know that, for happy bird `H`, there exist values of `x` and `y` such that `H(x) === y` and `H(y) === x`. That means we can swap out `y` for `H(x)`:

```js
H(H(y)) === y;
```

And, under the composition condition, we know there exists a bird that composes `H` with itself:
```js
const composed = compose(H, H);
```
We invoke `composed` with `y` and unpack the composition:
```js
composed(y); // => H(H(y));
```
Now, we already know that `H(H(y)) === y`, so we also know that `composed(y) === y`. Thus, `composed` is fond of `y`, and there's at least one normal bird in the forest.

[**Next =>**](../9/README.md)
