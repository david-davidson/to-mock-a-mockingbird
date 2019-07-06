### Problem
A Kestrel `K` might be fond of a Lark `L`. If this is the case, show that every bird is fond of `L`.

### Solution
We can easily show that this Lark is hopelessly egocentric:
```js
const K = x => y => x;
const L = x => y => x(y(y));

K(L) => L; // Assume `K` is fond of `L`
K(L)(x) => L(x); // Call both with another arbitrary bird, `x`
K(L)(x) => L; // From the Kestrel's definition
L(x) === L; // Hopelessly egocentric!
```

From there, we've already shown (in [#26](../26/README.md)) that, if a Lark is hopessly egocentric, every bird must be fond of it.

[**Next =>**](../29/README.md)
