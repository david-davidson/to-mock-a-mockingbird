# Egocentric?

### Conditions
A bird is considered "egocentric" if it is fond of itself: if, when called with itself, it responds with itself.

### Problem
Show that, under the conditions of the [previous problem's forest](../1/README.md), at least one bird is egocentric.

### Solution
We have already proved that every bird is fond of at least one other bird, and we know the forest contains a Mockingbird. So, we can assume there exists a bird `E` that the _Mockingbird_ is fond of.

Because the Mockingbird is fond of `E`, we know that `M(E)` evaluates to `E`. And from the Mockingbird's definition, we also know that `M(E)` evaluates to `E(E)`. For both to be true, `E` and `E(E)` must be the same. Thus, there exists a bird that is egocentric.
```js
M(E); // => E, from behavior of "fondness"
M(E); // => E(E), from definition of M
E === E(E);
```

[**Next =>**](../3/README.md)
