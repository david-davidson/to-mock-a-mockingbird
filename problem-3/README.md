# Story of the Agreeable Bird

### Conditions
* Two birds are said to "agree" on an input if both respond to that input with the same output
* A bird is "agreeable" if for every other bird, there is at least one input on which the two agree
* We're given the conditions of problem 1 (composition holds), but rather than a Mockingbird, the forest holds at least one agreeable bird

### Problem
Can we still show that every bird is fond of at least one bird?

(Bonuses: How is problem 1 nothing more than a special case of this problem? Is the Mockingbird agreeable?)

### Solution
We known there's at least one agreeable bird present; call it `A`. Under the composition condition, we can compose any arbitrary bird `x` with `A`
```js
let A; // The agreeable bird
const composed = compose(x, A);
```
Because `A` is agreeable, we know there is _some_ bird (call it `y`) on which `A` and `composed` agree.
```js
A(y) === composed(y);
```
Unpacking the composition, we can restate that as:
```js
A(y) === x(A(y));
```
Thus, bird `x` is fond of `A(y)`.

### Notes

The Mockingbird (`x => x(x)`) _is_ agreeable, because for any bird `x`, it agrees with `x` _on `x` itself_. So, because the Mockingbord is one of many possible agreeable birds, the conditions of problem 3 include those of problem 1, making it just a special case.
