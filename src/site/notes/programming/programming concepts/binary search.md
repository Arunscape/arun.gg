---
{"dg-publish":true,"permalink":"/programming/programming-concepts/binary-search/"}
---

- [[O(log(n))\|O(log(n))]]
- [[sorting algorithms\|sorting algorithms]]
```typescript
// assume it's ordered
function bs_list(haystack: number[], needle: number): boolean {

  if (haystack.length === 0)
    return false

  const i = Math.floor(haystack.length/2)
  const mid = haystack[i]

  if (mid === needle)
    return true
  else if (needle < mid)
    return bs_list(haystack.slice(0, i), needle)
  else
    return bs_list(haystack.slice(i+1, haystack.length), needle)
}

```