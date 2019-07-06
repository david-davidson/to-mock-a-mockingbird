### Problem
If there is a Lark in the forest, it follows that every bird is fond of at least one bird. Why?

### Solution
We start from the definition of the Lark:
```js
L(x)(y) => x(y(y));
```

Now, for `y`, swap in `L(x)`:
```js
L(x)(L(x)) => x(L(x)(L(x)));
```
Voilà! `x` is fond of `L(x)(L(x))`. (Smullyan notes that this general fact will be useful for later problems.)

[**Next =>**](../26/README.md)
