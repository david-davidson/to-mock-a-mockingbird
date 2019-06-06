# Another Fact about Kestrels

### Problem
Prove that for any Kestrel `K` and any bird `x`, if `K` is fond of `K(x)`, then `K` is fond of `x`.

### Solution
Our premise is that `K` is fond of `K(x)`:
```js
K(K(x)) => K(x);
```
And our conclusion is that `K` is fond of `x`:
```js
K(x) => x;
```
So how do we get there? Recall that the Kestrel fixates on its first argument. From `K(K(x)) => K(x)`, it's true that 1.) `K(K(x))` is fixated on `K(x)` and 2.) `K(x)` is fixated on `x`. But `K(K(x))` and `K(x)` are the _same bird_, (the first evaluates to the second), which means a single bird is fixated on both `K(x)` and `x`. That means `K(x)` and `x` are the same bird, or `K(x) => x`—therefore, `K` is fond of `x`.

[**Next =>**](../19/README.md)
