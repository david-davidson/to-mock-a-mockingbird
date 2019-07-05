### Conditions
A bird `L` is called a `Lark` if, for any birds `x` and `y`, the following condition holds:
```js
L(x)(y) => x(y(y))
```

### Problem
Prove that if the forest contains a Lark `L` and an Identity bird `I`, it must also contain a Mockingbird `M`.

### Solution
`L(x)` returns a Mockingbird! It evaluates to `y => I(y(y))`, which (because the Identity bird doesn't modify its argument) is the same as `y => y(y)`.

[**Next =>**](../25/README.md)
