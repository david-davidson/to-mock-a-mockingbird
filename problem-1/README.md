# The Significance of the Mockingbird

### Conditions
* The "Mockingbird" is a function that, for every argument `x`, returns `x(x)`
* Composition operates on two functions (birds) at a time: `compose(A, B)` evaluates to `A(B(x))`
* One bird is considered "fond" of another if, when the first is called with the second, the first responds _with_ the second

### Problem
Smullyan proposes a forest where 1.) there exists a Mockingbird and 2.) the "composition condition" holds, such that for any two birds `A` and `B`, there exists a bird `C` that composes the two. In this forest, is it the case that every bird is "fond" of any least one other?

### Solution
Under Smullyan's conditions, we can compose any arbitrary bird `A` with the Mockingbird:
```js
const M = x => x(x); // Mockingbird
const composed = compose(A, M);
```
From there, we can call `composed` _with itself_. Under the hood, this is the same as calling `A(M(composed))`.
```js
composed(composed) === A(M(composed));
```
Now, given the definition of the Mockingbird, we can evaluate `M(composed)` to `composed(composed)`:
```js
composed(composed) === A(composed(composed));
```
And given that `composed(composed)` and `A(composed(composed))` are equivalent, we can observe that `A` is fond of `composed(composed)`. Thus, for any arbitrary bird `A`, the answer to Smullyan's question is *yes*: `A` is fond of at least one other bird.

### Notes
We can't actually evaluate `composed(composed)` in JavaScript without a stack overflow, since the composed Mockingbird creates an infinite recursive series: `composed(composed)` => `A(M(composed))` => `A(composed(composed))` => `A(A(M(composed)))` => `A(A(composed(composed)))`... However, the observation that `composed(composed)` and `A(composed(composed))` are equivalent follows from pure logic. Thus, we can say something true about the program without actually being able to run it.

Smullyan, in laying out the problem, hints that the solution is "based on a principle that derives ultimately from the work of the logician Kurt Gödel." As far as I can tell, what he's getting at is the notion of making claims about an entire uncounted (/uncountable) set by proposing a series of 1:1 transformations on each entry. The Gödel connection comes from Gödel's incompleteness theorem, which makes the (early) claim that every statement in a given formal language can be mapped, via an arbitrary transformation, to a natural number. Here, the arbitrary transformation is the mapping of each bird to a truth claim, which allows us to make general statements about the forest.

