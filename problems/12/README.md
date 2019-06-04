# Another Fact about Kestrels

### Problem
Prove that for any Kestrel `K` and any bird `x`, if `K(x)` is egocentric, then `K` must be fond of `x`.

### Solution
We start with a `K(x)` that is egocentric:
```js
K(x)(K(x)) => K(x);
```
But because the Kestrel fixates on its first argument, that same expression must also return `x`:
```js
K(x)(K(x)) => x;
```
Therefore, `K(x)` and `x` are the same bird, and if `K(x) === x`, `K` is fond of `x`.

[**Next =>**](../13/README.md)
