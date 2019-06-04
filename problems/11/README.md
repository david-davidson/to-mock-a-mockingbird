# A Fact about Kestrels

### Problem
Prove that if a Kestrel is egocentric, it must be hopelessly egocentric.

### Solution
If a Kestrel `K` is egocentric, it returns itself when called with itself:
```js
K(K) => K;
```
But `K(K)` is itself fixated on `K`, because the Kestrel fixates on its first argument:
```js
K(K)(y) => K; // where `y` is any arbitrary bird
```
Since `K(K)` and `K` are the same bird, we can simplify that to:
```js
K(y) => K;
```
And voilà—this Kestrel is hopelessly egocentric!

### Notes

Smullyan boils the proof down to even simpler terms: per [problem 9](../9/README.md), any bird that the Kestrel is fond of is hopelessly egocentric. An egocentric Kestrel is fond of itself, and thus hopelessly egocentric.

[**Next =>**](../12/README.md)
