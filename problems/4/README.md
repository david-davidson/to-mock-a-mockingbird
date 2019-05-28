# A Question on Agreeable Birds

### Conditions
`A`, `B`, and `C` are birds such that `C` composes `A` with `B`.

### Problem
Show that, if `C` is agreeable, so is `A`.

### Solution
Assume an arbitrary bird `D`. We don't know anything about it, but we want to show that `A` and `D` agree on some bird.

Given `D`, we can assume _another_ arbitrary bird that composes `D` with `B`:
```js
const composed = compose(D, B);
```
Because `C` is agreeable, it and `composed` agree on at least one bird; call it `x`:
```js
C(x) === composed(x);
```
When we unpack `composed`, we get:
```js
C(x) === D(B(x));
```
And when we unpack `C` (recall, also composed), we get:
```js
A(B(x)) === D(B(x));
```
That is, `A` and `D` agree on the bird `B(x)`. Since `D` is arbitrary, this holds no matter its value; thus, `A` is agreeable.

[**Next =>**](../5/README.md)
