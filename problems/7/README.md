# Happy Birds

### Conditions
* The conditions of [problem 6](../6/README.md) hold
* We note that, in the definition of compatibility, `A` and `B` might be the _same_ bird (compatible with itself), or the `x` and `y` inputs might be the _same_ value
* A bird that is compatible with itself is called "happy": that is, for happy bird `A`, there exist birds `x` and `y` such that `A(x) === y` and `A(y) === x`

### Problem
* Show that any bird that is fond of another must be happy

### Solution
This one's simple. Recall that bird `A` is fond of bird `x` when `A(x) === x`, and that, in the definition of compatibility, `x` and `y` may be the same bird. `A(x) === x` automatically satisfies both `A(x) === y` and `A(y) === x` when `x` and `y` are the same. Thus, `A` will be compatible with itself, and happy.

[**Next =>**](../8/README.md)
