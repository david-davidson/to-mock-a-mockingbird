# Hopelessly Egocentric

### Conditions
* Recall that a bird is [egocentric](../2/README.md) when it responds to itself with itself: `x(x) => x`. A bird is "hopelessly egocentric" if, no matter _what_ you call it with, it always responds with itself: `x(<anything>) => x`.
* A bird is "fixated" on another if, given any input, it responds with that input. (That is, a bird that is hopelessly egocentric is one that is fixated on itself.)
* The Kestrel is a bird where, for any values of `x` and `y`, `K(x)(y) => x`. (That is, `K(x)` is fixated on `x`.)

### Problem
As with [problem 1](../problem-1/README.md), composition holds, and the the forest contains a Mockingbird. It also contains a Kestrel. Show that at least one bird is hopelessly egocentric.

### Solution
The individual conditions of problem 1 are a red herring—you don't need to (as I first tried) somehow compose the Mockingbird and the Kestrel. Instead, it's a _consequence_ of problem 1 that's important: the fact that, under its conditions, every bird is fond of at least one other.

That means the Kestrel is fond of another bird—call it `A`:
```js
K(A) === A;
```
Since those two are equivalent, so are the results of calling each with another arbitrary bird, `x`:
```js
K(A)(x) === A(x);
```
But since the Kestrel is fixated on its first argument, `A`, we know that `K(A)(x)` always returns `A`. Given that `K(A)(x)` is equivalent to both `A(x)` and `A`, we can state that `A` is hopelessly egocentric: it always returns itself.
```js
// Both true:
K(A)(x) === A;
K(A)(x) === A(x);
```
