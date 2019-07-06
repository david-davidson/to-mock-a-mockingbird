### Conditions
The forest contains a Lark `L`.

### Problem
With no other information, we can prove that at least one bird in the forest must be egocentric. How?

### Solution
This one's complicated! Definitely needed to skip to Smullyan's explanation.

From [#25](../25/README.md), we know that every bird is fond of at least one bird. Suppose that `L(L)` is fond of `y`.

Therefore, `L(L)(y) => y`, but also (from the Lark's definition) `L(L)(y) => L(y(y))`. Therefore, `L(y(y)) === y`.

Applying each side to `y` _again_, that means that `L(y(y))(y) === y(y)`—but also, from the Lark's definition, `L(y(y))(y) => y(y)(y(y))`. Since `y(y) === y(y)(y(y))`, `y(y)` is egocentric!
