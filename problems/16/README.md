# Another Fact about Kestrels

### Problem
In general, it is _not_ true that if `A(x) === A(y)`, `x === y`. However, it _is_ true if `A` is a Kestrel. Show that if `K(x) === K(y)`, then `x === y`.

### Solution
Given that `K(x) === K(y)`, it's also the case that `K(x)(z) === K(y)(z)`, where `z` is any arbitrary bird. But `K(x)(z)` is equal to `x`, and `K(y)(z)` is equal to `y`, so `x === y`.

[**Next =>**](../17/README.md)
