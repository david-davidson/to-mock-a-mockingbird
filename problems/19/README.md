# A Riddle

### Problem
Someone once said, "any egocentric Kestrel must be extremely lonely." Why is this true?

### Solution
We want to show that a Kestrel that's egocentric must be, by definition, the only bird in the forest. My proof differs slightly from Smullyan's.

From [problem 11](../11/README.md), we know that if a Kestrel is egocentric, it is _hopelessly_ egocentric:
```js
K(x) === K; // For any bird `x`
```
If we call both birds with any bird `y`, the left side of the equation will fixate on `x`:
```js
K(x)(y) === x;
```
But the right side (`K(y)`) will evaluate to `K`, because `K` is hopelessly egocentric. Therefore, for every bird `x`, `x` and `K` are the same bird. Thus, `K` is the only bird in the forest.

### Notes
Smullyan's two proofs start from the same place: the notion that a Kestrel that's egocentric is hopelessly egocentric.

In the first proof, we take any two birds `x` and `y`, and note that K's response to both is the same (`K`).
```js
K(x) => K;
K(y) => K;
K(x) === K(y);
```
From [problem 16](../16/README.md), we know that if `K(x) === K(y)`, then `x === y`.

The second proof is similar to mine, but doesn't need a second bird `y`. First, we consider `K(x)` for every bird `x`. It's fixated on `x` (because it's a Kestrel), and it evaluates to `K` (because it's hopelessly egocentric). Therefore, `K` is fixated on `x` (and, still, on `K`). From [problem 17](../17/README.md), we know that a bird cannot be fixated on more than one bird—thus, every value of `x` is the _same_ bird as `K`, and `K` is the only bird in the forest.
